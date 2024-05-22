##### Create database:
```sql
CREATE DATABASE test;
```

##### Delete database:
```sql
DROP DATABASE IF EXISTS test;
```

###### if has connection to db check with `force`
```sql
DROP DATABASE dbname WITH (FORCE);
```

```sql
dropdb -f dbname
```


##### Alter database name
```sql
ALTER DATABASE db_name_now RENAME TO db_name_new;
```
