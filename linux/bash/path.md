## PATH

```sh
PATH="${PATH:+${PATH}:}~/opt/bin"
```

in file `~/.profile`
```sh
# paste
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
export PATH=$PATH:$GOPATH/bin:/usr/local/go/bin
```
