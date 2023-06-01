# Git ssh


## create key

```sh
ssh-keygen -t rsa -b 4096 -C "{email}"
```

copy pub key to service

check
```sh
ssh -T -i {path_to_private_key}
```

In a file  `~/.ssh/config`
```
Host github.com
    IdentityFile ~/.ssh/{private_key}
```

check
```sh
ssh -T git@{repo}
 ```
