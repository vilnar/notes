## Export Gnome Terminal Profile

List profiles

```sh
dconf dump /org/gnome/terminal/legacy/profiles:/
```

Determine the terminal profile string for the profile you will need. This is the terminal profile that I will export:

```
[:741ee6ba-652f-4e14-8619-d34eaada40f7]
background-color='rgb(255,255,255)'
bold-color-same-as-fg=true
bold-is-bright=false
cursor-blink-mode='off'
cursor-colors-set=false
default-size-columns=100
foreground-color='rgb(0,0,0)'
palette=['rgb(0,0,0)', 'rgb(170,0,0)', 'rgb(6,141,6)', 'rgb(170,85,0)', 'rgb(0,0,170)', 'rgb(170,0,170)', 'rgb(24,105,105)', 'rgb(167,167,167)', 'rgb(85,85,85)', 'rgb(218,105,105)', 'rgb(56,241,56)', 'rgb(246,246,55)', 'rgb(85,85,255)', 'rgb(255,85,255)', 'rgb(88,241,241)', 'rgb(255,255,255)']
text-blink-mode='never'
use-theme-colors=false
use-theme-transparency=false
visible-name='light'
```

And the string that I will need to use to export is

```
:741ee6ba-652f-4e14-8619-d34eaada40f7
```

The command to export that profile is (note the ending slash)

```sh
dconf dump /org/gnome/terminal/legacy/profiles:/:741ee6ba-652f-4e14-8619-d34eaada40f7/ > gnome-terminal-dark2-profile.dconf
```

To restore the profile

```sh
dconf load /org/gnome/terminal/legacy/profiles:/:741ee6ba-652f-4e14-8619-d34eaada40f7/ < gnome-terminal-light-profile.dconf
```
