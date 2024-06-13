### invalid byte sequence for encoding "UTF8":
this throws any errors like below:
###### when you try restore with [[restore db#use `pg_restore`]]:
```
pg_restore: error: input file does not appear to be a valid archive
```

and

###### when you try restore with [[restore db#use `psql`]]:
```
ERROR:  invalid byte sequence for encoding "UTF8": 0xff
ERROR:  syntax error at or near ""
LINE 1: 0A=>5 5  =8O 154.nK :8 5=85 A>2KE...
        ^
......
ERROR:  syntax error at or near ""
LINE 1: ;
        ^
ERROR:  invalid byte sequence for encoding "UTF8": 0xfc
ERROR:  invalid byte sequence for encoding "UTF8": 0xbb
ERROR:  syntax error at or near ""
LINE 1: > A5 =KE s:0>1H8@=>9  n0te:.N ,4 6diawbo6k4...
        ^
ERROR:  syntax error at or near ""
LINE 1: 59.B5;
        ^
.....
```

# SOLUTION
first check encoding of backup file with command:
```sh
file backuped.sql
```
it show you file details:
```
backup.sql: Unicode text, UTF-16, little-endian text, with very long lines (5240), with CRLF line terminators
```

then check here encoding showed UTF-16, but you need utf-8. and to convert use `iconv` commands:
```
iconv -f UTF-16 -t utf-8 backup.sql > converted_utf8.sql
```

This command creates new `converted_utf8.sql` file and you can successfully restore this file using: [[restore db]]