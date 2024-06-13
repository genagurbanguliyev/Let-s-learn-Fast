> [!tip] in ubuntu terminal

### sign in to psql console:
```shell
$ sudo su postgres
or
$ sudo -i -u postgres

# type your password then type below:

postgresql$ psql
```

### list databases & tables
######  show all databases `psql> \l`
###### connect to specific db: `psql> \c <database_name>`
###### show all tables : 
 - Method 1: Using the `\dt` (list tables) command
 - Method 2: Using the `information_schema.tables` system view:
```SQL
Method 1
psql> \c database_name  # Connect to the database
psql (desired_database_name)> \dt;

 your_table_name                         public | TABLE  | your_table_name |
 another_table_name                      public | TABLE  | another_table_name |
 ... (other tables in the database)

=======================================
Method 2
psql> \c desired_database_name  # Connect to the database

psql (desired_database_name)> SELECT table_name FROM information_schema.tables;

  table_name
-------------
 your_table_name
 another_table_name
 ... (other tables in the database)
 ```

#### show the columns in a table:
```sql
psql> \c desired_database_name # Connect to the database psql (desired_database_name)> \d your_table_name;
```
