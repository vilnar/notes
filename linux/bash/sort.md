```
sort --key 2 --numeric-sort {filename}
```

## examples
```
$ cat {filename}
A 12
B 48
C 3

$ sort --key 2 --numeric-sort {filename} 
C 3
A 12
B 48
```
