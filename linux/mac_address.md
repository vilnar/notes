## set new mac address

```sh
ip link ls
sudo ip link set dev {interface_name} down
sudo ip link set dev {interface_name} address {new_mac_address}
sudo ip link set dev {interface_name} up
```


## Revert

```sh
ip link ls
sudo ip link set dev {interface_name} down
sudo ip link set dev {interface_name} address {old_mac_address}
sudo ip link set dev {interface_name} up
```
