## ANALYZE

The `EXPLAIN` command prints the execution plan of a query without executing it.

The plan contains the order of the operations, join methods, index usage, and estimated costs:

```sql
EXPLAIN {query}
```

The `ANALYZE` command collects statistics about the data in a table or index.

In opposite to the EXPLAIN command, it provides actual runtime performance metrics:
```sql
ANALYZE {table-name} (column1, column2, …)
```

You can also combine both commands to get the complete insight into query optimization and fine-tuning in PostgreSQL:
```sql
EXPLAIN ANALYZE {query}
```

time
```sql
\timing
```
