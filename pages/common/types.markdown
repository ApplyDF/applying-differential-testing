---
layout: minimal
title: Data Types
parent: Common SQL Changes
nav_order: 6
---

# Data Types

| _ID_ | _Name_  | _Difference_ | _Action Taken_ | _DBMS_                  | _Description_                  |
| :--- | :------ | :----------- | :------------- | :---------------------- | :----------------------------- |
|      | INTEGER | Semantic     | Remove         | Postgres, SQLite        | Has different size             |
|      | TEXT    | Semantic     | Remove         | MySQL, Postgres, SQLite | Cannot be used as primary keys |
|      | REAL    | Semantic     | Remove         | Postgres, SQLite        | Has different size             |
|      | NUMERIC | Semantic     | Remove         | SQLite                  | Has different size             |
