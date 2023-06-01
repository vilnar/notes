## count all the lines in directory recursive

```sh
find . -type f -exec wc -l {} \; | awk '{ SUM += $0} END { print SUM }'
```


## count by file type

```sh
find . -name '*.[ch]' | xargs wc -l
find . -name '*.el' | xargs wc -l
```
