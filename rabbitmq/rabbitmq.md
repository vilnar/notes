## API

```sh
curl --include --user guest:guest -X GET http://{host}:{port}/api/queues


curl --include --user guest:guest -X PUT http://{host}:{port}/api/vhosts/apilogs
rabbitmqctl add_vhost apilogs
```


```sh
curl --include --user guest:guest -X GET http://{host}:{port}/api/vhosts
```



## create queue

```sh
rabbitmqadmin declare queue --vhost=apilogs --user=guest --password=guest name=api_logs durable=true
rabbitmqctl list_queues -p apilogs
```

```sh
rabbitmqadmin list queues
```
