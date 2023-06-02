## install gdb

```sh
sudo apt update && sudo apt-get -y install gdb
```

## commands

```
break {file:num}
run
info locals
print {var}
q

help all
```

## breakpoints

```
# save
(gdb) save breakpoints my.brk
# restore
(gdb) source my.brk
```


## tui

```
https://www.youtube.com/watch?v=RPeHpRYvnqU
https://www.youtube.com/watch?v=YzIBwqWC6EM
```

`C-x a`

```sh
g++ -g gdb.cpp -o prog
gdb --tui ./prog
```
