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



## how to export and import database in postgres

To export and import a PostgreSQL database, you can use command-line tools like `pg_dump` for exporting and `psql` for importing. Here's how to do both:

### Exporting a PostgreSQL Database
To export a PostgreSQL database to a file, you can use the `pg_dump` utility. Here's the basic syntax:

```sql
pg_dump -U username -W -F t database_name > database_file.tar
```
- `-U username`: Specifies the PostgreSQL user.
- `-W`: Prompts for the password of the user.
- `-F t`: Specifies the output file format. In this case, `t` stands for TAR file format, which is suitable for database backups.
- `database_name`: The name of the database you want to export.
- `database_file.tar`: The name of the file where the exported database will be saved.

For example, to export a database named `mydatabase` to a file named `mydatabase_backup.tar`, you would run:

```sql
pg_dump -U myuser -W -F t mydatabase > mydatabase_backup.tar
```

### Importing a PostgreSQL Database
To import a database from a file, you can use the `psql` utility. Here's how:
First, create a new database where you'll import the data:
`createdb -U username database_name`
Then, import the data using `pg_restore` for TAR files:

```sql
pg_restore -U username -d database_name -1 database_file.tar
```
Or, if you exported the database in SQL format (using `-F p` option with `pg_dump`), you would use `psql` instead:

```sql
psql -U username -d database_name < database_file.sql
```
In both cases:

- `-U username`: Specifies the PostgreSQL user.
- `-d database_name`: Specifies the name of the database where the data will be imported.
- `database_file.tar` or `database_file.sql`: The path to the file containing the exported database.

Remember to replace `username`, `database_name`, and `database_file.tar` or `database_file.sql` with your actual PostgreSQL username, the name of your database, and the path to your backup file.
***

# ERRORS
 - [[restore error|invalid byte sequence for encoding "UTF8"]]