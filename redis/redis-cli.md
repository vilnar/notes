## CLI

```sh
sudo apt install redis-tools
```

```sh
redis-cli
```

```
AUTH password
```

```sh
redis-cli -h {host} -p {port} -a {password}
redis-cli -h {host} -p {port} ping
redis-cli -h {host} -p {port} -a {password} ping
redis-cli -u redis://{password}@{host}:{port}
redis-cli -u redis://{username}:{password}@{host}:{port}
```

```
FLUSHALL
```


```
KEYS *
KEYS key*
```

```sh
for key in `echo 'KEYS *type_key*' | redis-cli -h 127.0.0.1 -p {port} -a 'pasword' | awk '{print $1}'`
    do echo DEL $key
done | redis-cli -h 127.0.0.1 -p {port} -a 'password'
```




## get value

```
GET {key}
```

## get time

```
TTL {key}
```
