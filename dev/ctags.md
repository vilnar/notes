## Genarate

generate for project
```sh
ctags `find . -name "*.go" -print && find . -name "*.proto" -print`
```

generate for file
```sh
ctags -f - --sort=no --excmd=number commands.md
```
