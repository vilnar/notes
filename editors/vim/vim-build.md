## pre-install

remove apt vim
```sh
sudo apt remove vim vim-runtime gvim vim-tiny vim-common vim-gui-common vim-nox gvim
```

pre-install package
```sh
sudo apt install git make clang libxt-dev libgtk-3-dev libpython3-dev python3-dev libtool-bin gettext libncurses5-dev libncursesw5-dev build-essential
```


## default install

from project root directory
```sh
cd vim/src && make && sudo make install
```

## remove

```sh
sudo make uninstall
```


## build custom

from project root directory
```sh
make clean && make distclean

./configure \
--with-features=huge \
--enable-cscope \
--enable-multibyte \
--enable-python3interp=yes \
--with-python3-config-dir=$(python3-config --configdir) \
--enable-gui=auto \
--enable-gtk3-check \
--enable-gnome-check \
--with-x \
--enable-largefile \
--prefix=/usr/local \
--enable-terminal

# make -j4 VIMRUNTIMEDIR=/usr/local/share/vim/vim82
# j4 - use core count, check by `nproc`
make -j4 VIMRUNTIMEDIR=/usr/local/share/vim/vim90
sudo make install
```


## fix gvim desktop

```sh
sudo mkdir -p /usr/local/share/icons/hicolor/48x48/apps
sudo mkdir -p /usr/local/share/icons/locolor/32x32/apps
sudo mkdir -p /usr/local/share/icons/locolor/32x32/apps
sudo mkdir -p /usr/local/share/icons/locolor/16x16/apps
sudo mkdir -p /usr/local/share/applications
```
