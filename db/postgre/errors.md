## pg_dump: error

pg_dump: error: query failed: ERROR:  permission denied for sequence
```sql
GRANT USAGE, SELECT ON SEQUENCE blabla_seq TO postgres;
```
