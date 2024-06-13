##### Restore db from `sql` file:

###### use `pg_restore`
```sql
pg_restore -h localhost -p 5432 -U postgres -d my_new_database my_old_database.backup
```

###### use `psql`:
```sql
psql -h localhost -U postgres -p 5432 my_new_database < my_old_database.backup
```
where `-h` host, `-p` port, `-u` login username, `-d` name of database


***

# ERRORS
 - [[restore error|invalid byte sequence for encoding "UTF8"]]