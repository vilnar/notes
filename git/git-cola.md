## requirements

```sh
sudo apt install python3.10-venv
sudo apt install python3-pip
```

maybe
```sh
sudo apt-get remove qt5*
```

## install (warning: not work)

```sh
git checkout {tag}
```

build
```sh
python3 -m venv --system-site-packages env3
source env3/bin/activate
# make requirements-dev requirements-optional
# make develop
make prefix=$HOME/.local install

# check $PATH
# git-cola


# remove
make prefix=$HOME/.local uninstall
```
