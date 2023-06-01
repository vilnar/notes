# Vim info

Editor cheat sheet

## Get lines info

`C-g`

## Vim - count lines in selected range

`gC-g`

## navigate history

`C-o` jumping back
`C-i` jump forward

## undo/redo

`u` - undo
`C-r` - redo


## go to bash

`C-z` - pause vim
`fg` - return vim


## window

### create window

`C-w n`

### slit window emtpy
```
:vs new
```

### move between windows

`C-w h/j/k/l`

### move window

`C-w H/J/K/L`

### close all window

`C-w q`


## editing

`c a w` - remove word
`d` - remove with copy/cut

### navigate by char

```
f-{search_char} - goto next char in line
F-{search_char} - goto back char in line
; - goto next char
```

`%` - goto pair symbol

`t-{search_char}` - goto before char

example:
`dt'` - delete all to '


## marks

goto last change in file
```
`.
```

### goto mark

```
`-{mark_char}
```

### mark local

```
m-{one_char}
```

### mark global create

```
m-{one_char_caps_lock}
```

## goto file under cursor

```
g-f
```

## grep and quickfix

```
grep -rni '{search_phrase}' {path}
:copen
:cn
:cp
```

## vimgrep

```
:vimgrep {search_phrase} {path}
:vimgrep def *
:cnext
:cprev
```

Examples:
```
:vimgrep /text/ path_to_dir/* path_to_dir/**/*
:vimgrep /foo/j **/*.md
```

## goto line

```
{line_number}-gg
```


## Switching case of characters

Uppercase "HellO" to "HELLO" with `gU` then a movement.
Lowercase "HellO" to "hello" with `gu` then a movement.


## Complete

`C-p`, `C-n`  - prev, next
`C-y`, `C-e`  - select, cancel


## tabs

```
:tabs
:tabnew
:file empty_tab_name
:sav path_to_save_empty_tab
```


## search and replace

### find with count match

```
:%s/pattern//ng
```

### simple replace all

```
%s/foo/bar/g
```

### replace with ask for confirm

add flag `c`
```
%s/foo/bar/gc
```

### replace with non-regex

```
:%sno/search_string/replace_string/gnc
```

### replace example

add `||test` to the end of each line
```
%s/$/||test/g
```

## replace last search

```
%s//test/gc
```

## replace whole word

```
%s/\<word\>/newword/g
```

replace and case sensitive
```
:%s/\<word\>\C/newword/g
```

```
* - search next word in cursor
# - search prev word in cursor
:noh - disable highlight search
```

Find next, previous - `n`, `N`


## Ex mode
### paste in ex mode

```
<C-r>+
```

### find command in history

```
:<C-f>
```

## VISUAL LINE

press in normal mode `V`


## select

### reselect the last selection quickly

```
gv
```

### highlight html tags

```
vat
vit
```

## fold

Commands for control
`zc` - collapse block
`zo` - expand block
`zm` - close all blocks
`zr` - open all blocks
`za` - inverting (if open - close, if closed - open)
`zj` - go to the next convolution
`zk` - go to the previous convolution
`zF` - create fold


## wrap and move in multiline

`gj`
`gk`


## diff

```
vsplit
diffthis
```

## term

```
:vert terminal
```


## set encode

```
:help encoding-names
```

## detect encode and save with encode

```
:!chardet3 %
:set fileencoding=iso-8859-5
:w
```

## open with encode

```
:e ++enc=ISO-8859-5 {file_path}
```

open this file
```
:e ++enc=ISO-8859-5 %
```

show support encoding list
```
:help encoding-values
```

## command-line effectively

`q/` and `q:` and return `ctrl-c`


## fix indentation

`=` is an operator


## Find and Replace within selection (visual)

press `:`
you'll see something like this appear in the command line:
```
:'<,'>
```

Then type s/foo/bar/c
```
:'<,'>s/foo/bar/c
```

## find within selection

```
'<,'>g/foo/#
```

## netrw copy path

`mf`
`mx`
`ls`

## terminal in vim

switch to 'Terminal-Normal mode' with `C-w N`

## abbrev

In insert mode, type {keys} then press `Ctrl-]`

## buffer delete range

```
:3,5bd[elete]
```
Will delete buffer range from 3 to 5 .

## spell

```
:setlocal spell spelllang=uk
```

bad word suggest
`z=`

Add word under the cursor as a good word to the first name in 'spellfile'.
`zg`

## macros

repeat in normal mode
```
10@q
```

## get func list

```
:help function-list
```

## help func under cursor

Press `K` in normal mode


## vim server

open files in one terminal
```
vim --servername project1 --remote .vimrc
vim --servername project1 --remote .bash_aliases
```

## easy mod

With -y (easy mode), Vim defaults to insert mode, and you cannot permanently exit to normal mode via `<Esc>`.

However, like in default Vim, you can issue a single normal mode command via `<C-O>`. So to exit, type `<C-O>:q!<CR>`.

Alternatively, there's a special `<C-L>` mapping for easy mode that returns to normal mode

## exit from insert mode

`ctrl-[` or `ctrl-c` or `esc`

## colors

`:help term_setansicolors`
```
		The colors normally are:
			0    black
			1    dark red
			2    dark green
			3    brown
			4    dark blue
			5    dark magenta
			6    dark cyan
			7    light grey
			8    dark grey
			9    red
			10   green
			11   yellow
			12   blue
			13   magenta
			14   cyan
			15   white
```

```
so $VIMRUNTIME/syntax/colortest.vim
```

## range

```
put = range(11,15)
```


## fugitive

```
G diff --name-status master...
Gvdiffsplit master...
Gtabedit master
G log -n 1000
```

From `:h fugitive-mappings` you can use:
```
<cr> to open the diff in the current window
o open the diff in a horizontal split
O to open the diff in a new tab page
S open diff in a vertical split
I imagine you want to use S on the diff line. However as screen space can be a concern with diff-ing, O might be a better option.
```

## tips

swap two characters
```
xp
```

### unicode

in insert mode `C-v` and press code and `ESC`
```
<C-v>u00b7
```

show unicode under cursor
in normal mode `ga`
