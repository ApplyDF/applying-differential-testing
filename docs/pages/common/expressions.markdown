---
layout: minimal
title: Expressions
parent: Common SQL Changes
nav_order: 7
---

# Expressions

| _ID_ | _Name_                | _Difference_ | _Action Taken_ | _DBMS_                  | _Description_                                                              |
| :--- | :-------------------- | :----------- | :------------- | :---------------------- | :------------------------------------------------------------------------- |
|      | ~                     | Semantic     | Remove         | SQLite                  | MySQL has different default type for bit wise operation                    |
|      | <<                    | Semantic     | Remove         | MySQL, SQLite           | MySQL has different default type for bit wise operation                    |
|      | >>                    | Semantic     | Remove         | MySQL, SQLite           | MySQL has different default type for bit wise operation                    |
|      | &                     | Semantic     | Remove         | MySQL, SQLite           | MySQL has different default type for bit wise operation                    |
|      | \|                    | Semantic     | Remove         | MySQL, SQLite           | MySQL has different default type for bit wise operation                    |
|      | LENGTH                | Semantic     | Remove         | Postgres, SQLite        | SQLite counts differently with multibyte characters                        |
|      | SUBSTR                | Semantic     | Remove         | Postgres, SQLite        | MySQL behaves differently with negative position value                     |
|      | Division operator (/) | Semantic     | Remove         | Postgres, SQLite        | MySQL divides differently with INT                                         |
|      | NULL value            | Semantic     | Add            | SQLite                  | Add option to disable null value, some expressions handle null differently |
|      | Integer value         | Semantic     | Modify         | Postgres, SQLite, MySQL | Limit the maximum generated integer                                        |
|      | Special string value  | Semantic     | Remove         | Postgres                | "TRUE", "FALSE", "infinity" string have semantic meaning in Postgres       |
|      | Negative value        | Semantic     | Modify         | SQLite                  | Modify to disable negative value for some expression                       |
|      | Infinity              | Semantic     | Remove         | SQLite                  | Remove 1e500 as it is illegal value for MySQL                              |
|      | COLLATE               | Semantic     | Remove         | SQLite, Postgres        | There are no common collations                                             |
|      | LIKE                  | Semantic     | Add            | MySQL, SQLite, Postgres | add default escape for LIKE operator                                       |
