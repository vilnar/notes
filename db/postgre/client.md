## install PostgreSQL 13 client

WARNING: now work for debian 10
```sh
sudo apt update
curl https://www.postgresql.org/media/keys/ACCC4CF8.asc | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/apt.postgresql.org.gpg >/dev/null
echo "deb [arch=amd64] http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main" | sudo tee /etc/apt/sources.list.d/postgresql.list
sudo apt update
sudo apt install postgresql-client-13
```



## remove
```sh
sudo rm /etc/apt/trusted.gpg.d/apt.postgresql.org.gpg
sudo rm /etc/apt/sources.list.d/postgresql.list
sudo apt update
sudo apt install postgresql-client
```
