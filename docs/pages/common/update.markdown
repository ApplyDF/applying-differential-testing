---
layout: minimal
title: UPDATE
parent: Common SQL Changes
nav_order: 4
---

# UPDATE

| _ID_    | _Name_                        | _Difference_            | _Action Taken_ | _DBMS_                      | _Description_                                                                      |
| :------ | :---------------------------- | :---------------------- | :------------- | :-------------------------- | :--------------------------------------------------------------------------------- |
| **U01** | **DEFAULT keyword**           | **Syntactic**           | **Remove**     | **MySQL, Postgres**         |                                                                                    |
|         |                               |                         |                |                             |                                                                                    |
| **U02** | **Uncommon update syntax**    | **Syntactic, Semantic** | **Remove**     | **MySQL, Postgres, SQLite** |                                                                                    |
|         | duplicate update to a column  | Syntactic               | Remove         | SQLite                      | Example: UPDATE t0 SET c0=1, c0=2;                                                 |
|         | multiple columns update       | Syntactic               | Remove         | SQLite                      | Example: UPDATE t0 SET (c0, c1)=(1,2);                                             |
|         | column as the value to update | Semantic                | Remove         | MySQL, Postgres             | MySQL get new col value every small update, but SQLite,Postgres get col value once |
|         |                               |                         |                |                             |                                                                                    |
| **U03** | **Other spefic options**      | **Syntactic**           | **Remove**     | **SQLite**                  |                                                                                    |
|         | OR IGNORE                     | Syntactic               | Remove         | SQite                       |                                                                                    |
|         | OR ROLLBACK                   | Syntactic               | Remove         | SQLite                      |                                                                                    |
|         | OR ABORT                      | Syntactic               | Remove         | SQLite                      |                                                                                    |
|         | OR REPLACE                    | Syntactic               | Remove         | SQLite                      |                                                                                    |
|         | OR FAIL                       | Syntactic               | Remove         | SQLite                      |                                                                                    |
