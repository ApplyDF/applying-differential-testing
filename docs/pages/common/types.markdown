---
layout: minimal
title: Data Types
parent: Common SQL Changes
nav_order: 6
---

# Data Types

| _ID_ | _Name_  | _Difference_ | _Action Taken_ | _DBMS_                  | _Description_                                              | _Related Links_                                                                                                                                                             |
| :--- | :------ | :----------- | :------------- | :---------------------- | :--------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|      | INTEGER | Semantic     | Remove         | Postgres, SQLite        | SQLite treat it as 8 bytes, others treat it as 4 bytes     | https://dev.mysql.com/doc/refman/8.4/en/integer-types.html<br>https://www.postgresql.org/docs/current/datatype-numeric.html<br>https://www.sqlite.org/datatype3.html        |
|      | TEXT    | Semantic     | Remove         | MySQL, Postgres, SQLite | Cannot be used as primary keys in MySQL                    | https://dev.mysql.com/doc/refman/8.4/en/column-indexes.html                                                                                                                 |
|      | REAL    | Semantic     | Remove         | Postgres, SQLite        | PostgreSQL treat it as 4 bytes, others treat it as 8 bytes | https://dev.mysql.com/doc/refman/8.4/en/floating-point-types.html<br>https://www.postgresql.org/docs/current/datatype-numeric.html<br>https://www.sqlite.org/datatype3.html |
|      | NUMERIC | Semantic     | Remove         | SQLite                  | SQLite ignores the size specification                      | https://www.sqlite.org/datatype3.html                                                                                                                                       |
