## SSH tunnels and port forwarding

```sh
ssh -L 0.0.0.0:7777:{host_postgres}:{port_postgres} -L 0.0.0.0:8888:{host_sphinx}:{port_sphinx} {user_ssh}@{ip_ssh} -p {port_ssh}
```

## debug client

```sh
ssh -vv user@host
ssh -vvv user@host
```

## key

```sh
ssh -i {path_to_key} user@host
```

## generate key

```sh
ssh-keygen -t rsa -b 4096 -C "{your_email}"
```

## generate key without answers

```sh
ssh-keygen -t rsa -b 4096
ssh-keygen -t rsa -b 4096 -f ./id_rsa_replica
```

## permission

```sh
chmod 0700 ~/.ssh && chmod 0600 ~/.ssh/authorized_keys
chmod 0600 ~/.ssh/*
chmod 0644 ~/.ssh/*.pub
```


## server

```sh
/etc/ssh/sshd_config
sudo systemctl restart ssh
```

### debug server

```sh
systemctl stop sshd
/usr/sbin/sshd -d
```


## copy ssh key

```sh
ssh-keygen -t rsa -b 4096 -f {path_to_ssh_key}
```
Приватний залишається

Публічний `*.pub` ключ копіюється на сервер, який потрібно додати в файл `authorized_keys`
Якщо вручну:
```sh
cat >> ~/.ssh/authorized_keys

ssh-copy-id -i ~/.ssh/public_key user@host
```

## log

```
/var/log/auth.log
```
