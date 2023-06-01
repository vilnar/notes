## hasura

graphql hasura Postgres: Filter query results / search queries

https://hasura.io/docs/latest/graphql/core/databases/postgres/queries/query-filters.html#jsonb-operators-contains-has-key-etc

## Equality operators (`_eq, _neq`)

The `_eq` (equal to) or the `_neq` (not equal to) operators are compatible with any Postgres type
other than json or jsonB (like Integer, Float, Double, Text, Boolean, Date/Time/Timestamp, etc.).


## Greater than or less than operators (`_gt, _lt, _gte, _lte`)

The `_gt` (greater than), `_lt` (less than), `_gte` (greater than or equal to), `_lte` (less than or equal to) operators are compatible 
with any Postgres type other than json or jsonB (like Integer, Float, Double, Text, Boolean, Date/Time/Timestamp, etc.).

## List based search operators (`_in, _nin`)

The `_in` (in a list) and `_nin` (not in list) operators are used to compare field values to a list of values. 
They are compatible with any Postgres type other than json or jsonB (like Integer, Float, Double, Text, Boolean, Date/Time/Timestamp, etc.).

## Text search or pattern matching operators (`_like, _similar`, etc.)

The `_like, _nlike, _ilike, _nilike, _similar, _nsimilar, _regex, _nregex, _iregex, _niregex` operators are used for pattern 
matching on string/text fields.

## JSONB operators (`_contains, _has_key`, etc.)

## Filter or check for null values (`_is_null`)

`_gt` (greater than)
`_lt` (less than)
`_gte` (greater than or equal to)
`_lte` (less than or equal to)
`_in` (equal to)
`_not_in` (not equal to)
