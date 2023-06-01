## Створення/Запуск і вхід в контейнер

```sh
docker run -it nginx bash
```

## Запуск контейнера і виконання команди cat в середині

```sh
docker run nginx cat /etc/nginx/nginx.conf
```
Запуск nginx, не повертає управління.

## Запуск команди в контейнері

```sh
docker exec {id_or_name_container} sh -c "cat /etc/hosts"
```

## Порт

прокинути порт 8080 ззовні контейнера в контейнер на порт 80
```sh
docker run -p 8080:80 nginx
```

## Видалити image

-f (force)
```sh
docker rmi {image_name}
```

## Видалити контейнер

```sh
docker rm {id_or_name}
```

## Видалити volume

```sh
docker volume rm {volume_name}
```

## створити volume

```sh
docker volume create --name={volume_name}
```

## Запуск nginx в фоні. Флаг -d

```sh
docker run -d -p 8080:80 nginx
```

## вивід логів

```sh
docker logs {id_or_name_container}
```

## підключитись до виводу логів в стілі tail -f

```sh
docker logs -f {id_or_name_container}
```

## логи в файл

```sh
docker logs {id_or_name_container} > output.log
docker logs {id_or_name_container} | tee output.log
```

## Інформація про запущені контейнери

```sh
docker ps
```

## скільки русурсів займають запущені контейнери

```sh
docker stats
```

## зупинити контейнер

```sh
docker kill {id_or_name}
docker stop {id_or_name}
```

## start

```sh
docker start {id_or_name}
```

## volumes доступ до файлової системи(фс)

`-v`

Шлях з основної фс до `:` після внутрішній шлях (контейнер)
```sh
docker run -it -v ~/.bash_history:/root/.bash_history ubuntu bash
```

## env

-e
```sh
docker run -it -e "HOME=/tmp" ubuntu bash
```

## build

```sh
docker build -t {new_image_name} {path_to_dockerfile_folder}
docker run -p 8080:8080 -v {local_project_path}:{path_in_container} -d --tty --name {new_container_name} {image_name}
```

## stop auto-start container after system reboot

```sh
docker update --restart no {container_name}
```

## clear containers

```sh
docker rm -f $(docker ps -a -q)
```

## host.docker.internal

172.17.0.1

## docker image show content

```sh
docker images
docker image history --no-trunc {image_id} > image_history
```


## docker copy from container to local

```sh
docker cp {container}:{SRC_PATH} {DEST_PATH}
```
