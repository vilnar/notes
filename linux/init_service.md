## services

service
```sh
service {service_name} status
service {service_name} start
service {service_name} stop
```

systemctl
```sh
systemctl status {service_name}
systemctl start {service_name}
systemctl stop {service_name}
systemctl restart {service_name}
```

init.d
```sh
/etc/init.d/{service_name} status
/etc/init.d/{service_name} start
/etc/init.d/{service_name} stop
```
