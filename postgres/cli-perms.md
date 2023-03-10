**Grant CONNECT to the database:**

`GRANT CONNECT ON DATABASE database_name TO username;`

**Grant USAGE on schema:**

`GRANT USAGE ON SCHEMA schema_name TO username;`

**Grant on all tables for DML statements: SELECT, INSERT, UPDATE, DELETE:**

`GRANT SELECT, INSERT, UPDATE, DELETE ON ALL TABLES IN SCHEMA schema_name TO username;`

**Grant all privileges on all tables in the schema:**

`GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA schema_name TO username;`

**Grant all privileges on all sequences in the schema:**

`GRANT ALL PRIVILEGES ON ALL SEQUENCES IN SCHEMA schema_name TO username;`

**Grant all privileges on the database:**

`GRANT ALL PRIVILEGES ON DATABASE database_name TO username;`

**Grant permission to create database:**

`ALTER USER username CREATEDB;`

**Make a user superuser:**

`ALTER USER myuser WITH SUPERUSER;`

**Remove superuser status:**

`ALTER USER username WITH NOSUPERUSER;`

**Those statements above only affect the current existing tables. To apply to newly created tables, you need to use alter default. For example:**

````ALTER DEFAULT PRIVILEGES
FOR USER username
IN SCHEMA schema_name
GRANT SELECT, INSERT, UPDATE, DELETE ON TABLES TO username;```
````
