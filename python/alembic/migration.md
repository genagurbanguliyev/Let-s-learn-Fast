#migration
###### Migration
###### makemigration:
```shell
alembic revision --autogenerate -m "init"
```

###### migrate:
```shell
alembic upgrade head
```

###### show migrations as SQL:
```shell
alembic upgrade head --sql
```
