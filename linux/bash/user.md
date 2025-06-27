## create user

```sh
useradd -m john
passwd john
# check
id john
```


add home directory
```sh
mkhomedir_helper john
```

login
```sh
su - john
```


bash
```sh
usermod -s /bin/bash john
```
