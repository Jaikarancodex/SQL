# SQL
# Relational Database Basics
A structured collection of data organized into tables that relate to each other via keys. It enforces consistency with rules (constraints) and lets you query with SQL.
#### Table ≈ spreadsheet.
#### Row (record) ≈ one item/entry.
#### Column (field/attribute) ≈ a property of the item.
#### Primary Key (PK): uniquely identifies a row.
#### Foreign Key (FK): points to a PK in another table to represent relationships.

## Types of relationships
#### 1–1: one row maps to one row (rare).
#### 1–many: a department has many employees (common).
#### many–many: students and courses (needs a junction table).

# DBMS (MySQL, Postgres, SQL Server)
A DBMS stores data, enforces rules, and runs SQL.

#### MySQL: very popular, great for web apps.
#### PostgreSQL: feature-rich, strong standards compliance.
#### SQL Server: Microsoft ecosystem, enterprise features.

# Basic SQL Syntax
General patterns:
###
<img width="1450" height="158" alt="image" src="https://github.com/user-attachments/assets/e21c44a9-16c5-4f4f-8f88-b300f9e22d48" />

##### Case-insensitive for keywords (SELECT = select).
##### Strings use single quotes 'text'.
##### End statements with ;.

