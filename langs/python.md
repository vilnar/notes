## ubuntu 20.04 install python2

```sh
sudo apt-get install python
```


## install pip

```sh
curl https://bootstrap.pypa.io/pip/2.7/get-pip.py --output get-pip.py
python get-pip.py
```


## fix

/usr/bin/env: ‘python’: No such file or directory
```sh
which python
which python3
ln -s /usr/bin/python3 /usr/bin/python
```


## youtube-dl

https://addons.mozilla.org/en-US/firefox/addon/cookies-txt/

install latest version

pip install git+https://github.com/ytdl-org/youtube-dl.git@master#egg=youtube_dl

```sh
python -m youtube_dl -o "~/Downloads/%(title)s.%(ext)s" --cookie "~/Downloads/cookies.txt" "https://www.youtube.com/watch?v=id"
```

## where is python.h located

```
python3
>>> import sysconfig
>>> sysconfig.get_path('include')
'/usr/include/python3.10'
```


```sh
ld -lpython3.10 --verbose
ld -L/usr/lib/python3.10/config-3.10-x86_64-linux-gnu -L/usr/lib/x86_64-linux-gnu -lpython3.10 --verbose
```


## install package

```sh
pip install {package}
```

from source
```sh
git clone {link}
cd {project}
pip install -e .
```

```sh
pip uninstall {package}
```
