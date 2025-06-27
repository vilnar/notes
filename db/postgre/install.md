## Install postgresql

```sh
sudo apt update && sudo apt upgrade
sudo apt install postgresql postgresql-contrib
sudo systemctl status postgresql
sudo systemctl start postgresql
sudo systemctl stop postgresql
```

## Basic setup

```sh
sudo -u postgres psql
```

add access
```
sudo -u postgres psql

CREATE USER buzz with password 'hostmancloud';
CREATE DATABASE cloud_db
GRANT ALL PRIVILEGES ON DATABASE cloud_db TO buzz;
ALTER DATABASE cloud_db OWNER TO buzz;
```
