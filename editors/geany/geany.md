## NEW

see `geany/geany-plugins/.github/workflows/build.yml`
```sh
sudo apt install ccache libtool libgtk-3-dev autopoint gettext intltool check cppcheck
sudo apt install libctpl-dev liblua5.1-0-dev libgpgme-dev libgtkspell-dev libgtkspell3-3-dev
sudo apt install libsoup2.4-dev libgit2-dev libxml2-dev
sduo apt install libmarkdown2-dev libwebkit2gtk-4.1-dev
sduo apt install libvte-2.91-dev libenchant-2-dev
```


```sh
./configure --disable-html-docs && make && sudo make install
```

install by meson
```sh
rm -rf build build-aux
mkdir build; cd build; meson ..
cd ..
meson compile -C build
sudo meson install -C build
```


## install plugins

```sh
./configure --enable-spellcheck --enable-debugger --enable-markdown && make && sudo make install
./configure && make && sudo make install
```

## install themes

```sh
bash install.sh
```
