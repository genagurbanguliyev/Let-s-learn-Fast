##### Restore db from `sql` file:
Below is my version of `pg_dump` which I use to restore the database:

```sql
pg_restore -h localhost -p 5432 -U postgres -d my_new_database my_old_database.backup
```

or use `psql`:
```sql
psql -h localhost -U postgres -p 5432 my_new_database < my_old_database.backup
```
where `-h` host, `-p` port, `-u` login username, `-d` name of database
