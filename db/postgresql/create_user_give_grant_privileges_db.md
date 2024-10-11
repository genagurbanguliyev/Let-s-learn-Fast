---
Technology: database
tags:
  - postgres
  - sql
  - privileges
created_at: 2024-10-11
---
### Create new role(user)
First login and go sql console with:
`sudo su postgres` -> `psql`
or  `psql -U postgres`

###### Create new user
```sql
create user <myuser> with encrypted password 'password';
```
<small>This command creates user with name "myuser"</small>

###### Give grant privileger:
```sql
grant all privileges on database <db_name> to <my_user>;
```
<small>This command give all privileges to "myuser" for "db_name" database</small>
