## export table limit rows

```sql
CREATE TABLE {forum_export} as SELECT * FROM forum LIMIT 50000;
```

### export database

```sh
pg_dump --data-only --host 127.0.0.1 --port 5432 --username postgres --dbname mydb  > backup
pg_dump --data-only --host {host} --port {port} --username {user_name} --dbname {data_base} > {file_path}
```

### export table

```sh
pg_dump --host {host} --port {port} --username {user_name} --dbname {data_base} --table {table} --file {file_path}
```

### import

```sh
psql --host {host} --port {port} --username {user_name} --dbname {data_base}  < {file_path}
```


### dump table and restore data only

```sh
pg_dump --host {host} --port {port} --username {user_name} --dbname {db_name} --data-only --table {table_name} > {path_to_file}
psql --host {host} --port {port} --username {user_name} --dbname {data_base}  < {file_path}
```
