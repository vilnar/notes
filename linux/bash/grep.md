## find in file types

```sh
grep -rn --include="*.php" "findPhrase" .
grep -rn --include=*.{ts,js,json} "findPhrase" .
```

## grep for special characters

```sh
grep -e '->'
```

## Get number of lines matching a pattern in a file

```sh
grep -c "pattern" my_text_file.txt
```


## exclude by directories names

```sh
grep -rn --exclude-dir=node_modules 'some_pattern' /path/to/search
grep -rn --exclude-dir={node_modules,dir1,dir2,dir3} 'some_pattern' /path/to/search
```

## COMBO find and grep, exclude by direcotries path

```sh
find . -type f -not -path "./vendor/*" -not -path "./runtime/*" -not -path "./web/*" -not -path "./test/*" -not -path "./views/*" -not -path "./widgets/*" | xargs grep "YII_" -nH
```

## show lines before and after the match

```sh
grep -B 4 'keyword' /path/to/file.log
grep -A 2 'keyword' /path/to/file.log
```


## escape slash

```sh
printf '<%s>\n' G "G" 'G' \G "\G" '\G' \\G "\\G" '\\G'
```
