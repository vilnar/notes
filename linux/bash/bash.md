## special variables

```
Special		Variable Description

$0		The name of the bash script.

$1, $2...$n	The bash script arguments.

$$		The process id of the current shell.

$#		The total number of arguments passed to the script.

$@		The value of all the arguments passed to the script.

$?		The exit status of the last executed command.

$!		The process id of the last executed command.
```

## conditions

```
-eq # Equal
-ne # Not equal
-lt # Less than
-le # Less than or equal
-gt # Greater than
-ge # Greater than or equal
```

## compare strings

```sh
if [ "$output" = "" ]; then
    # ...
fi
if [ "$output" != "" ]; then
    # ...
fi
```


## scripts

```sh
for i in {1..60}; do
	echo "sleep second ${i}"
	sleep 1
done
```

## special sign
`>` - перезаписати файл
`>>` - в кінець файлу

## multiple commands to file

```sh
{ cmd1 && cmd2 && cmd3; } > file
```

## escape single quote

```sh
echo 'abc'\''abc'
# abc'abc


echo "abc"\""abc"
# abc"abc
```
