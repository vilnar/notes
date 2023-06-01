## View current locks

```sql
SELECT relation::regclass as relname,pid,relation,locktype,database,mode,granted,fastpath FROM pg_locks;
```

## Killing locks

```sql
SELECT pg_cancel_backend({pid});
```


## test

```sql
SELECT l.pid FROM pg_locks l JOIN pg_class c ON l.relation = c.oid AND c.relkind = 'r' WHERE c.relname = '{table_name}';
```
