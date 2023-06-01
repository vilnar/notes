# Resurce

## перегляд занятого місця

```sh
df -h
```

## перегляд занятого місця на диску

```sh
df -h | grep /dev/sd
```

## розмір дирикторії

```sh
du -h -s /var/www/
```

## розмір поточної дирикторії

```sh
du -h -s *
```

## читаємий розмір файлу для ls

```sh
ls -lah
```

## від сортувати директорії та файли по розміру

```sh
du -sh -- *  | sort -rh
```

## limites

```sh
ulimit -a
```


## disk io

```sh
sudo iotop
```

## check ssd or hard disk

for column `ROTA (rotational device)` - `1` for hard disks and `0` for a SSD
```sh
df -h
lsblk
lsblk -d -o name,rota
```

## check ssd health

```sh
sudo apt-get install smartmontools
df -h
lsblk
sudo smartctl -i /dev/sdX
sudo smartctl -t short -a /dev/sdX
sudo smartctl -a /dev/sdX | grep -n "Percentage"
sudo smartctl -a /dev/sdX | grep -n "Power_On_Hours"
sudo smartctl -a /dev/sdX | grep -n "Wear_Leveling_Count"


hdparm -tT /dev/sdX
```

## cpu info

```sh
cat /proc/cpuinfo  | grep 'name'| uniq
cat /proc/cpuinfo  | grep process| wc -l


ps -eo pcpu,pid,user,args | sort -r -k1 | less
```
