
##### backup specific table from database:
```
pg_dump -U <username> -W -F c -b -v -f "path/to/backup_file.tar" <database_name> -t <table_name> 
```

##### restore specific table from database:
```
pg_restore -U <username> -d <database_name> -t <table_name> "/path/to/backup.tar"
```
