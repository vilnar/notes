# Connect

## local

```sh
psql --username {user} --dbname {database}
```

## external

```sh
psql --host {host} --port {port} --username {username} --dbname {database}
psql postgresql://login:pass@host:port/base
```

## port

6432 - pgbouncer
5432 - postgres
