## burn iso image to usb drive in linux

1. before create `fat` partition by gnome-disk-utility
2. unmount usb
3. run commands

```sh
lsblk

sudo dd bs=4M if={path_to_iso_file} of=/dev/{sda} status=progress oflag=sync
sudo dd bs=4M if={path_to_iso_file} of=/dev/{sda} conv=fdatasync status=progress
```
