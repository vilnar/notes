## create symlinks

powershell
```
New-Item -ItemType SymbolicLink -Path 'C:\Users\{username}\vimfiles' -Target 'D:\Code\dotfiles\vim'
New-Item -ItemType SymbolicLink -Path 'C:\cygwin64\home\{username}\.vim' -Target 'D:\Code\dotfiles\vim'
```

cmd
```
mklink RUN.exe bin\RUN.exe
```

## statup

win+r
regedit.exe
```
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
```


win+r
shell:startup


## youtube download

```
yt-dlp.exe -P "D:/Downloads" -o "%(title)s.%(ext)s" SK1G9FmZlhY&si=ffhJVZWuHQ1b1w2h --cookies "D:/Downloads/cookies.txt"
yt-dlp.exe -P "D:/Downloads" -o "%(title)s.mp3" a28uIPLJrLw&si=AJ6Ja8Z_wO2fUUDp --cookies "D:/Downloads/cookies.txt"
```

## kill vmmem

open powershell by admin
```
wsl --shutdown
```

## hosts

```
c:\Windows\System32\drivers\etc\hosts
```
