---
layout: minimal
title: INSERT
parent: Common SQL Changes
nav_order: 3
---

# INSERT

| _ID_    | _Name_                     | _Difference_  | _Action Taken_ | _DBMS_               | _Description_                          | _Related Links_                                                                                                |
| :------ | :------------------------- | :------------ | :------------- | :------------------- | :------------------------------------- | :------------------------------------------------------------------------------------------------------------- |
| **I01** | **Priority modifiers**     | **Syntactic** | **Remove**     | **MySQL**            |                                        |                                                                                                                |
|         | LOW_PRIORITY               | Syntactic     | Remove         | MySQL                | Not supported by PostgreSQL and SQLite | https://dev.mysql.com/doc/refman/8.4/en/insert.html                                                            |
|         | DELAYED                    | Syntactic     | Remove         | MySQL                | Not supported by PostgreSQL and SQLite | https://dev.mysql.com/doc/refman/8.4/en/insert.html                                                            |
|         | HIGH_PRIORITY              | Syntactic     | Remove         | MySQL                | Not supported by PostgreSQL and SQLite | https://dev.mysql.com/doc/refman/8.4/en/insert.html                                                            |
|         | IGNORE                     | Syntactic     | Remove         | MySQL                | Not supported by PostgreSQL and SQLite | https://dev.mysql.com/doc/refman/8.4/en/insert.html                                                            |
|         |                            |               |                |                      |                                        |                                                                                                                |
| **I02** | **Upsert clause**          | **Syntactic** | **Remove**     | **Postgres, SQLite** |                                        |                                                                                                                |
|         | ON CONFLICT                | Syntactic     | Remove         | Postgres, SQLite     | Not supported by MySQL                 | https://www.postgresql.org/docs/current/sql-insert.html<br>https://www.sqlite.org/syntax/upsert-clause.html    |
|         | DO NOTHING                 | Syntactic     | Remove         | Postgres, SQLite     | Not supported by MySQL                 | https://www.postgresql.org/docs/current/sql-insert.html<br>https://www.sqlite.org/syntax/upsert-clause.html    |
|         | UPDATE SET                 | Syntactic     | Remove         | SQLite               | Not supported by MySQL                 | https://www.postgresql.org/docs/current/sql-insert.html<br>https://www.sqlite.org/syntax/upsert-clause.html    |
|         |                            |               |                |                      |                                        |                                                                                                                |
| **I03** | **DEFAULT keyword**        | **Syntactic** | **Remove**     | **Postgres**         | **Not supported by SQLite**                | **https://dev.mysql.com/doc/refman/8.4/en/insert.html<br>https://www.postgresql.org/docs/current/sql-insert.html** |
|         |                            |               |                |                      |                                        |                                                                                                                |
| **I04** | **Other specific options** | **Syntactic** | **Remove**     | **Postgres, SQLite** |                                        |                                                                                                                |
|         | OR IGNORE                  | Syntactic     | Remove         | SQLite               | Not supported by MySQL and PostgreSQL  | https://www.sqlite.org/syntax/insert-stmt.html                                                                 |
|         | OR REPLACE                 | Syntactic     | Remove         | SQLite               | Not supported by MySQL and PostgreSQL  | https://www.sqlite.org/syntax/insert-stmt.html                                                                 |
|         | OR ABORT                   | Syntactic     | Remove         | SQLite               | Not supported by MySQL and PostgreSQL  | https://www.sqlite.org/syntax/insert-stmt.html                                                                 |
|         | OR FAIL                    | Syntactic     | Remove         | SQLite               | Not supported by MySQL and PostgreSQL  | https://www.sqlite.org/syntax/insert-stmt.html                                                                 |
|         | OR ROLLBACK                | Syntactic     | Remove         | SQLite               | Not supported by MySQL and PostgreSQL  | https://www.sqlite.org/syntax/insert-stmt.html                                                                 |
|         | OVERRIDING USER VALUE      | Syntactic     | Remove         | Postgres             | Not supported by MySQL and SQLite      | https://www.postgresql.org/docs/current/sql-insert.html                                                        |
|         | OVERRIDING SYSTEM VALUE    | Syntactic     | Remove         | Postgres             | Not supported by MySQL and SQLite      | https://www.postgresql.org/docs/current/sql-insert.html                                                        |
