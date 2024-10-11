---
Technology: database
tags:
  - postgres
  - sql
created_at: 2024-10-11
---
### Working with tables
###### remove all tables in database
```sql
DO $$ DECLARE 
	r RECORD; 
BEGIN
	FOR r IN (SELECT tablename FROM pg_tables WHERE schemaname = current_schema()) LOOP
	EXECUTE 'DROP TABLE IF EXISTS ' || quote_ident(r.tablename) || ' CASCADE';
	END LOOP;
END $$;
```