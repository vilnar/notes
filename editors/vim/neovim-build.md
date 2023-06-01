## prepare

```sh
sudo apt install ninja-build gettext libtool libtool-bin autoconf automake cmake g++ pkg-config unzip curl doxygen
sudo apt-get install ninja-build gettext libtool-bin cmake g++ pkg-config unzip curl
```


## install

<https://github.com/neovim/neovim/wiki/Installing-Neovim#uninstall>

```sh
sudo make -j4
sudo make install
```

or

```sh
sudo rm -r build/
make CMAKE_BUILD_TYPE=Release
sudo make install
```



```sh
sudo make uninstall
# or
sudo cmake --build build/ --target uninstall
```
