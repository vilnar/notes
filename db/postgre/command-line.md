# Command line PostgreSql

## exit

```
\q
```

## show tables

```
\d
```

## show schemes in database

```
\dn
```

## show tables structure

```
\d+ table_name
```

## output format

```
\x on
```

## Output format is unaligned

```
\a
```

## print only data from row, by new line

```sh
psql --host {host} --port {port} -t -A -F $'\n' -c "SELECT * FROM forum WHERE id IN (1)" > forum.txt
```

## print data for array php

```sh
psql --host {host} --port {port} -A -F ' => ' -c "\x" -c "SELECT * FROM forum WHERE id IN (4731475)" > forum.txt
```

## list of databases

```
\l
```

## permisson for table

```sql
SELECT grantee, privilege_type
FROM information_schema.role_table_grants
WHERE table_name='mytable';
```

or
```
\z "{table_name}"
```

or
```
\dt public.*
```

## Grant SELECT for a specific table

```sql
GRANT SELECT ON "{table_name}" TO {username};
```

## change owner

```sql
ALTER TABLE "{table_name}" OWNER TO {username};
```


## exec

```
--command="SELECT id FROM {table_name} LIMIT 500"
--command "SELECT id FROM {table_name} LIMIT 500"

# or file
--file={path_to_file}
```

## version

```sql
SELECT version();
```

## show null

```
\pset null '<null>'
```

## where your database data directory

```sh
show data_directory;
#        data_directory
# -----------------------------
#  /var/lib/postgresql/13/main
# (1 row)
```


## free space

Postgres не очищеє дані після DELETE, лише DROP

Щоб очистити вручну після DELETE потрібен pg_repack
```
pg_repack --table {table_name}
```
