# Emacs

## install new version on ubuntu

Download archive from official site
source `https://www.masteringemacs.org/article/speed-up-emacs-libjansson-native-elisp-compilation`
```sh
# Ubuntu 20.04.2 LTS (Focal Fossa)
sudo apt remove --autoremove emacs-common
sudo apt update
sudo apt install
sudo apt install -y autoconf make gcc texinfo gnutls-bin apt-transport-https ca-certificates curl gnupg-agent software-properties-common
apt-get install -y gcc-10 libgccjit0 libgccjit-10-dev

tar -zxvf emacs-28.2.tar.gz emacs-28.2
cd emacs-28.2

export CC=/usr/bin/gcc-10
./autogen.sh

./configure --with-native-compilation
make -j4
sudo make install
emacs
sudo make uninstall
```

## find directory or file

```
M-x find-name-dired
```

## tab indent

```
C-x TAB
```


## match brackets

```
C-M-n
C-M-p
```

## autoindent

mark whole buffer with `C-x h` (or M-x mark-whole-buffer)
run indent region with `C-M-\` (or M-x indent-region)


## search match count

```
M-s o
```

## Encode

set encode
`set-buffer-file-coding-system`

open a file with specific coding system
`revert-buffer-with-coding-system`

get current encoding system
M-x `describe-variable` (C-h v)
`buffer-file-coding-system`

## Jump to Previous Position

;; Create a mark and deactive it right away
`C-<SPC> C-<SPC>`

;; Jump back to the head of the mark-ring and pop it afterwards
`C-u C-<SPC>`

## jump buffer

`C-x left-arrow`
`C-x right-arrow`

## magit

### magit-blame

`magit-blame b`
`magit-show-commit`

## diff one file with other branch

`magit-diff`
`magit-diff-range` (action r)


## diff files

`ediff`
`ediff-buffers`

### ediff scroll sync

`scroll-all-mode`


## select column

`C-x SPC`


## sudo

Use `C-x C-f` and type out `/su::/etc/hosts` or `/sudo::/etc/hosts`


## Repeat selection after copy

`C-x C-x`


## macros

`f3` or` C-x (`
`f4` or` C-x )`

### set name for macros

M-x `name-last-kbd-macro`
or `C-x C-k n`

### run

M-x `name`


### find word under cursor

`M-s .`

## unsplit a particular window split

`C-x 0`


## count the number of lines in the region

`M-=` (command count-words-region)

## case change

`C-x C-u` uppercase
`C-x C-l` lowercase


## complete default

https://www.emacswiki.org/emacs/DynamicAbbreviations
```
M-/
```

## show you all bindings

`C-h b ` or M-x `describe-bindings`

## displaying recent keystrokes in emacs

`C-h l` or M-x `view-lossage`

## debug lisp

Debug in script
```lisp
(debug)
```

Debug by M-x
```
debug-on-entry
cancel-debug-on-entry
```

