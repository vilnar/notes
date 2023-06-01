## Ignore a Folders

```sh
rg --glob 'vendor' "custom_text" ./

# few folders ignore
rg --glob '!{vendor,runtime}' "custom_text" ./
```
