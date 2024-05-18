###### Create database:
```sql
CREATE DATABASE test;
```

***
###### delete database:
```sql
DROP DATABASE IF EXISTS test;
```

if has connection to db check with `force`

```sql
DROP DATABASE dbname WITH (FORCE);
```

```sql
dropdb -f dbname
```