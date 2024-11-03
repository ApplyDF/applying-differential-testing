---
layout: minimal
title: DELETE
parent: Common SQL Changes
nav_order: 5
---

# DELETE

| _ID_    | _Name_                 | _Difference_  | _Action Taken_ | _DBMS_              | _Description_                          | _Related Links_                                                                                        |
| :------ | :--------------------- | :------------ | :------------- | :------------------ | :------------------------------------- | :----------------------------------------------------------------------------------------------------- |
| **D01** | **Uncommon modifiers** | **Syntactic** | **Remove**     | **MySQL, Postgres** |                                        |                                                                                                        |
|         | LOW_PRIORITY           | Syntactic     | Remove         | MySQL               | Not supported by PostgreSQL and SQLite | https://dev.mysql.com/doc/refman/8.4/en/delete.html                                                    |
|         | QUICK                  | Syntactic     | Remove         | MySQL               | Not supported by PostgreSQL and SQLite | https://dev.mysql.com/doc/refman/8.4/en/delete.html                                                    |
|         | IGNORE                 | Syntactic     | Remove         | MySQL               | Not supported by PostgreSQL and SQLite | https://dev.mysql.com/doc/refman/8.4/en/delete.html                                                    |
|         | ONLY                   | Syntactic     | Remove         | Postgres            | Not supported by MySQL and SQLite      | https://www.postgresql.org/docs/current/sql-delete.html                                                |
|         |                        |               |                |                     |                                        |                                                                                                        |
| **D02** | **RETURNING clause**   | **Syntactic** | **Remove**     | **Postgres**        | **Not supported by MySQL**             | **https://www.postgresql.org/docs/current/sql-delete.html<br>https://www.sqlite.org/lang_delete.html** |
