---
layout: default
title: Found Bugs
nav_order: 6
---

# Found Bugs

This page lists out the bugs we found during our research.

---

## Two Single Quote Escaping Inconsistency
This is a verified bug in MySQL 8.1 where the system with 'NO_BACKSLASH_ESCAPES' mode enabled gives out error when using two single quotes in a single quote string expression. This error occurs only in expressions in some table constraints and index expressions. Using two double quotes works fine in any cases. 
```sql
SET sql_mode = 'NO_BACKSLASH_ESCAPES';
SELECT ''''; -- returns '
CREATE TABLE t0 (c0 TEXT CHECK(c0 = '''')); -- ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ''\'')'
CREATE TABLE t0 (c0 TEXT DEFAULT('''')); -- ERROR 1064 (42000): ... near ''\'')'
CREATE TABLE t0 (c0 TEXT GENERATED ALWAYS AS ('''')); -- ERROR 1064 (42000): ... near ''\'')'
SELECT """"; -- returns "
CREATE TABLE t0 (c0 TEXT CHECK(c0 = """")); -- QUERY OK

CREATE TABLE t0 (c0 INT);
CREATE INDEX i0 ON t0 (('''')); -- ERROR 1064 (42000): ... near ''\'')'
CREATE INDEX i0 ON t0 (("""")); -- QUERY OK
```
When the 'NO_BACKSLASH_ESCAPES' mode is disabled, the expressions are fine.
```sql
SET sql_mode = '';
SELECT ''''; -- returns '
CREATE TABLE t0 (c0 TEXT CHECK(c0 = '''')); -- QUERY OK
SELECT """"; -- returns "
CREATE TABLE t0 (c0 TEXT CHECK(c0 = """")); -- QUERY OK

CREATE TABLE t0 (c0 INT);
CREATE INDEX i0 ON t0 (('''')); -- QUERY OK
CREATE INDEX i0 ON t0 (("""")); -- QUERY OK
```
---

## Backslash Escaping Inconsistency in LIKE Operator
This is a verified bug in MySQL 8.3 where the system with 'NO_BACKSLASH_ESCAPES' mode enabled gives out error when escaping backslash ('\') in the LIKE operator. This error occurs only in expressions in some table constraints and index expressions.
```
SELECT 'a' LIKE 'a' ESCAPE '\'; -- returns 1
CREATE TABLE t0 (c0 BOOLEAN DEFAULT('a' LIKE 'a' ESCAPE '\')); -- ERROR 1210 (HY000): Incorrect arguments to ESCAPE
CREATE TABLE t0 (c0 BOOLEAN GENERATED ALWAYS AS ('a' LIKE 'a' ESCAPE '\')); -- Incorrect arguments to ESCAPE
CREATE TABLE t0 (c0 BOOLEAN, CHECK('a' LIKE 'a' ESCAPE '\')); -- Incorrect arguments to ESCAPE

CREATE TABLE t0 (c0 BOOLEAN);
CREATE INDEX i0 on t0 (('a' LIKE 'a' ESCAPE '\')); -- Incorrect arguments to ESCAPE
```