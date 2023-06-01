## Find

find file
```sh
find {path_to_find} -iname "*{file_name}*"
```

get files less than 16 megebyte
```sh
find . -size -16M -print
```

get files larger than 100 megabyte
```sh
find . -size +100M -print
```

find with exclude directories path
```sh
find . -type f -not -path "./vendor/*" -not -path "./runtime/*"
```

rename files by extension
```sh
find ./ -depth -name "*.md" -exec sh -c 'mv "$1" "${1%.md}.txt"' _ {} \;
```
