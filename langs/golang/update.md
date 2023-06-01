## old

```sh
sudo apt-get update
sudo apt-get -y upgrade

cd /tmp
wget https://dl.google.com/go/go1.14.2.linux-amd64.tar.gz
sudo tar -xvf go1.14.2.linux-amd64.tar.gz
rm go1.14.2.linux-amd64.tar.gz
go env
sudo mkdir /usr/lib/go-1.14.2
sudo mv go/* /usr/lib/go-1.14.2/
export GOROOT=/usr/lib/go-1.14.2
export GOTOOLDIR=/usr/lib/go-1.14.2/pkg/tool/linux_amd64
source ~/.profile
echo $GOROOT
ls -la /usr/bin/go
ls -la /usr/bin/gofmt
sudo rm /usr/bin/go /usr/bin/gofmt
sudo ln -s /usr/lib/go-1.14.2/bin/gofmt /usr/bin/gofmt
sudo ln -s /usr/lib/go-1.14.2/bin/go /usr/bin/go
ls -la /usr/bin/gofmt
ls -la /usr/bin/go
go version

#export GO111MODULE=on
```


## new version

```sh
sudo apt remove golang golang-golang-x-tools golang-1.13-go
sudo rm /usr/bin/go /usr/bin/gofmt


sudo apt update && sudo apt install build-essential -y
go version
cd /tmp

wget https://go.dev/dl/go1.19.4.linux-amd64.tar.gz
export PATH=$PATH:/usr/local/go/bin
sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf go1.19.4.linux-amd64.tar.gz

# add path
vim ~/.profile
# paste
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
export PATH=$PATH:$GOPATH/bin:/usr/local/go/bin
#
source ~/.profile

go install golang.org/x/tools/cmd/goimports@latest
```
