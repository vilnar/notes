## Change configs

```sh
sudo vim /etc/postgresql/{version}/main/pg_hba.conf
sudo /etc/init.d/postgresql reload
```

or
```sh
psql -U {user} {db} -h0
SELECT pg_reload_conf();
```



