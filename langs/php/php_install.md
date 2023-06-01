## install

pre install
```sh
sudo apt install -y pkg-config build-essential autoconf bison re2c libxml2-dev libsqlite3-dev libssl-dev libcurl4-openssl-dev libonig-dev libsodium-dev libzip-dev
```

```sh
tar -xzf php-8.1.13.tar.gz
cd php-8.1.13

./configure --with-openssl --enable-mbstring --with-curl --enable-calendar --enable-bcmath --enable-exif --enable-gd --enable-ftp --enable-pcntl --enable-sockets --with-sodium --with-zip --with-pear --enable-mysqlnd --with-pdo-mysql --with-zlib
```

Sometimes you may want to check how many cores your CPU has
```sh
nproc
```

```sh
make -j4
sudo make install
php -v
```
