## ubuntu

copy to `~/.local/share/fonts` and clear cache `sudo fc-cache -fv` or clear `sudo fc-cache`

## consolas

```sh
sudo apt install ttf-mscorefonts-installer
```

```sh
cd /tmp

# download
wget https://sourceforge.net/projects/mscorefonts2/files/cabs/PowerPointViewer.exe

# extract
cabextract -L -F ppviewer.cab PowerPointViewer.exe; cabextract -L -F "CONSOLA*.TTF" ppviewer.cab

# install

cp /tmp/consola*.ttf ~/.local/share/fonts
sudo chmod 644 ~/.local/share/fonts/consola*.ttf

sudo fc-cache -fv

# clean up
rm /tmp/consola*.ttf /tmp/PowerPointViewer.exe /tmp/ppviewer.cab
```


## size
Such rendering badly represents the actual look of the font, and that's why there are recommended font sizes:
```
6, 8, 9, 10, 11, 12, 14, 16, 18, 24, 30, 36, 48, 60, 72 px
```
