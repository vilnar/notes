# permission

## Find all recursive

```sh
find {path_to_dir} -type d -exec chmod 755 {} \;
find {path_to_dir} -type f -exec chmod 644 {} \;
```


## find by type

```sh
find {path/to/project} -name '*.css' -exec chmod 777 {} \;
```

## change own

```sh
sudo chown -R {user_name}:{user_group} {path}
sudo chmod -R 0777 {path}
```


## show user group

```sh
groups
groups {user_name}
```

## show users in group

```sh
getent group {user_name}
```

## login

```sh
sudo su - {user_name}
```

## run command from other user

```sh
sudo -u {user_name} {bash_command}
```

## allow executable permissions for user

```sh
chmod u+x {file}
chmod u+x {path}/*
```

## set read permissions for all

```sh
chmod a+r -R {dir_path}
```

## user id, group

```sh
echo $(id -u)
echo $(id -g)
```

change user id, group
```sh
usermod -u {user_id} {user_name}
groupmod -g {group_id} {user_name}
```

create user with id and group id
```sh
groupadd -g {group_id} {user_name}
useradd {user_name} -u {user_id} -g {group_id} -m -s /bin/bash
```


## add sudo all

```sh
echo "{user_name} ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
```

## add sudo nginx

```sh
echo "{user_name} ALL=(ALL) NOPASSWD: /usr/sbin/nginx -t,/usr/sbin/service nginx reload,/usr/sbin/service nginx restart" >> /etc/sudoers
```
