## Ubuntu Dock to show windows only from the current workspace

```sh
gsettings set org.gnome.shell.extensions.dash-to-dock isolate-workspaces true
```

## fix trash

```sh
gsettings set org.gnome.shell.extensions.dash-to-dock show-trash false
```

scroll fix
```sh
gsettings set org.gnome.shell.extensions.dash-to-dock scroll-action 'do-nothing'
```

## set default terminal

```sh
gsettings set org.gnome.desktop.default-applications.terminal exec gnome-terminal
gsettings set org.gnome.desktop.default-applications.terminal exec xterm
gsettings set org.gnome.desktop.default-applications.terminal exec kitty
gsettings set org.gnome.desktop.default-applications.terminal exec alacritty
```

## cursor blink

```sh
gsettings set org.gnome.desktop.interface cursor-blink false
```

## fix css color for vim

```
~/.config/gtk-3.0/gtk.css
```

```
window#vim-main-window {
    /* vim colorscheme zenburn  */
    background-color: #3F3F3F;
}
```

## flameshot

keyboars shortscut
command: flameshot gui
command: gnome-screenshot -a
ctrl+alt+insert

## gnome-vanilla-desktop

```sh
sudo apt install gnome-shell-extensions
```


## fix in ubuntu 22.04 ctrl+; (semicolon)

https://askubuntu.com/questions/1405311/ctrl-is-globally-bound-after-upgrading-to-ubuntu-22-04
```sh
ibus-setup
```
emoji tab, remove keyboard shortcuts


## applications locale

```sh
ls -lah /snap/firefox/current/firefox.desktop
ls -lah ~/.local/share/applications/
```

