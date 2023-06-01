## set local config from .gitconfig

work
```sh
git config user.email $(git config --get work.email)
git config user.name $(git config --get work.user)
```

personal
```sh
git config user.email $(git config --get personal.email)
git config user.name $(git config --get personal.user)
```

## show config

```sh
git config --list
git config --local --list
```
