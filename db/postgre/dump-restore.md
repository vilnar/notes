# dump or restore

## RESTORE

### restore database

```sh
pg_restore --host {host} --port {port} --username {user} --create --dbname {db_name} {path_to_file}
```

### restore table

```sh
pg_restore --host {host} --port {port} --username {user} --dbname {db_name} --table {table_name} {path_to_file}
```


## DUMP

### dump table in binary

```sh
pg_dump --host {host} --port {port} --username {user} --dbname {db_name} --table {table_name} --create --format c > {path_to_file}
```

### dump table in sql format

```sh
pg_dump --host {host} --port {port} --username {user} --dbname {db_name} --table {table_name} > {path_to_file}
```

few tables in one sql file
```sh
pg_dump --host {host} --port {port} --username {user} --dbname {db_name} --table {table_name_1} --table {table_name_2} > {path_to_file}
```

### dump schema only

```sh
pg_dump  --host {host} --port {port} --username {username} --dbname {db_name} --schema-only > {path_to_dump_file}
```

### COPY

copy dump select to file
```sh
psql --host {host} --port {port} --username {username} --dbname {db_name} -c 'COPY ({select_query}) TO STDOUT WITH CSV;' > {path_to_file}
```

copy from file
```sh
psql --host {host} --port {port} --username {username} --dbname {db_name} -c 'COPY "{table_name}" FROM STDIN (FORMAT csv);' < {path_to_file}
```
