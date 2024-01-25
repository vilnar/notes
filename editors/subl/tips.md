## Sublime - delete all lines containing specific value

```
^.*text*\n
```

## Select text between quotes

`ctrl+shift+space`


## quick add next

add `Ctrl+d`

skip `Ctrl+k Ctrl+d`

## select text in html tag

`ctrl+shift+a`


## exclude folders for search in files

```
-/{path}/,-/{path}/,-/{path}/,
```

## st4

```sh
echo test | subl -
```

```sh
subl --multiinstance --debug
subl --multiinstance
smerge --multiinstance
```

## debug

in console
```
sublime.log_commands(True)
sublime.log_input(True)
```

## download

```
https://www.sublimetext.com/3
https://www.sublimetext.com/dev
https://www.sublimetext.com/download


https://www.sublimemerge.com/dev
https://www.sublimemerge.com/download


https://download.sublimetext.com/sublime-text_build-4126_amd64.deb
https://download.sublimetext.com/sublime-merge_build-2068_amd64.deb

https://download.sublimetext.com/sublime-text_build-3211_amd64.deb
```

## smerge

diff between two commits
copy hashes from commits panel
press `ctrl+f`
```
commit:{hash1} or commit:{hash2}
```
select two commits

[source](https://github.com/sublimehq/sublime_merge/issues/255)
