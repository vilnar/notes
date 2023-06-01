# show ports

```sh
ss -tulpn | grep LISTEN


lsof -i -P -n | grep LISTEN

netstat -a -n | grep 15672
```
