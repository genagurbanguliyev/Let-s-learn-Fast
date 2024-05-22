###### truncate a table
```sql
TRUNCATE TABLE table_name;
```

###### truncate a table referenced in a foreign key constraint
You cannot `TRUNCATE` a table that has FK constraints applied on it (`TRUNCATE` is not the same as `DELETE`).

To work around this, use either of these solutions.

Simple way:
```sql
TRUNCATE TABLE table_name CASCADE;
```

or
```sql
SET FOREIGN_KEY_CHECKS = 0;

TRUNCATE table1;
TRUNCATE table2;

SET FOREIGN_KEY_CHECKS = 1;
```