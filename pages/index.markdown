---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Home
nav_order: 0
---

# Differential Testing for DBMSs
This is a supplementary website for the paper "On the Applicability of Differential Testing for Database Systems".

Additional examples and details of the differences between SQL dialects that hinder differential testing are provided here.

## Website Structure
This website is structured as follows:
- Uncommon SQL Changes
  - Statements
  - Data Types
  - Expressions
- Common SQL Changes
  - CREATE TABLE
  - SELECT
  - CREATE INDEX
  - INSERT
  - UPDATE
  - DELETE
  - Data Types
  - Expressions
- Different Behaviors
- Configurations Changed
- Found Bugs

**Uncommon SQL Changes** contains changes to SQLancer for uncommon features identified from the documentation analysis including *Statements*, *Data Types*, and *Expressions*.

**Common SQL Changes** contains changes to SQLancer for common features identified from the documentation analysis including *CREATE TABLE*, *SELECT*, *CREATE INDEX*, *INSERT*, *UPDATE*, *DELETE*, *Data Types*, and *Expressions*.

**Different Behaviors** shows an example of semantic discrepancies that initially looks like a bug, but they are intended.

**Configurations Changed** shows any configurations changed from the 3 DBMSs to be able to perform differential tesing consistently.

**Found Bugs** shows bugs found during our study on the paper.