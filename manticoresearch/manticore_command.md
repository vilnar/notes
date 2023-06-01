## client

```sh
apt-get install mariadb-client
```

## version

```sh
searchd -v
```

## status

```sh
indextool --check {index_name}
indextool --checkconfig --config {path}
```

```sh
mysql -h0 -P9306 -e "status"
```

`workers_clients` -  кількість реальних з'єднань
```sql
SHOW STATUS
```

потоки які є в даний момент
```sql
SHOW THREADS \G
```

```sh
mysql -h0 -P9306 -e "SHOW GLOBAL VARIABLES;"
```

```sql
SHOW GLOBAL VARIABLES;
SHOW INDEX search STATUS;
SHOW INDEX search SETTINGS;
```

## service

```sh
sudo -u manticore indextool --checkconfig --config {path_to_config}
sudo -u manticore searchd --stop --config {path_to_config}
sudo -u manticore searchd --config {path_to_config}

indexer --config {path_to_config} {index_name}
indexer --config {path_to_config} --all
indexer --config {path_to_config} --rotate --all
```

## query info

```sql
-- query ...
SHOW META;
```


## profiling

https://manual.manticoresearch.com/Profiling_and_monitoring/Profiling/Query_plan
```sql
SET profiling=1;

SELECT id FROM forum WHERE MATCH('i me') LIMIT 1;

SHOW PLAN;
```


## normalized

```sql
CALL KEYWORDS(
	'apple tv',
	'forum',
	1 as fold_wildcards,
	1 as fold_lemmas,
	1 as fold_blended,
	1 as stats
);
```

## ranker

```sql
SELECT id, PACKEDFACTORS(), title from search OPTION ranker = expr('1') \G;
```
