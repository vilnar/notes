## install binary

```sh
sudo mkdir /opt/kitty-0.25.2/
sudo tar -xvf kitty-0.25.2-x86_64.txz -C /opt/kitty-0.25.2/
sudo chown $USER:$USER -R /opt/kitty-0.25.2/
sudo ln -s /opt/kitty-0.25.2/bin/kitty /usr/local/bin/kitty
ln -s /opt/kitty-0.25.2/share/applications/kitty.desktop ~/.local/share/applications/kitty.desktop
ln -s /opt/kitty-0.25.2/share/applications/kitty-open.desktop ~/.local/share/applications/kitty-open.desktop
ln -s /opt/kitty-0.25.2/share/icons/hicolor/256x256/apps/kitty.png ~/.local/share/icons/hicolor/256x256/apps/kitty.png


# remove
sudo rm -rf /opt/kitty-0.25.2/
```



## install from source

```sh
sudo apt update
sudo apt remove kitty
sudo apt install git gcc cmake pkg-config libdbus-1-dev libxcursor-dev libxrandr-dev libxi-dev libxinerama-dev libgl1-mesa-dev libxkbcommon-x11-dev libfontconfig-dev libx11-xcb-dev liblcms2-dev libpython3-dev librsync-dev

make

sudo ln -s {full_path}/kitty/launcher/kitty /usr/local/bin/

remove
sudo rm /usr/local/bin/kitty
```
