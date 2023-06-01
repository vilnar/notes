## Delete All Files in a Directory Except One or Few Files

```sh
shopt -s extglob
rm -rf app/!(current)
rm -rf app/!("current"|"releases")
shopt -u extglob
```
