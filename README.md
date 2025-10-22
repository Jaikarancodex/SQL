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

# DDL — Data Definition Language
### CREATE, ALTER, DROP, TRUNCATE define or reshape schema.
## Step 1: Setup a practice database
###
<img width="1460" height="197" alt="image" src="https://github.com/user-attachments/assets/91a86ca8-337c-4eb3-b8fc-42a7a5cb2b9f" />

##  Step 2: Create Tables (CREATE)
###
<img width="1422" height="162" alt="image" src="https://github.com/user-attachments/assets/8bc5fca5-f0e6-4cd2-bf9f-9584f66ee42e" />

## Step 3: See the result
###
<img width="1463" height="162" alt="image" src="https://github.com/user-attachments/assets/a24ceb7e-d754-42c4-b3fa-83cf925c0dc0" />

## Step 4: Modify the Table (ALTER)
###
<img width="1442" height="182" alt="image" src="https://github.com/user-attachments/assets/4676edfb-af9c-4f20-b1b6-fb8cafd0277d" />
<img width="1456" height="130" alt="image" src="https://github.com/user-attachments/assets/edd292fb-3d3e-4265-9f3c-79692fc31f80" />

## Step 5: TRUNCATE TABLE
Removes all rows instantly and resets IDENTITY numbers.Structure and constraints stay — you can insert again.
###
<img width="1425" height="158" alt="image" src="https://github.com/user-attachments/assets/eec326fc-1c2f-487f-92e8-a650ff1ead55" />
<img width="1455" height="171" alt="image" src="https://github.com/user-attachments/assets/3b1073f0-0cd4-4ea2-8234-78880ea86acc" />

## Step 6: DROP TABLE or DATABASE
Completely removes object (data + definition).After drop, it’s gone — you can’t select from it again unless recreated.
###
<img width="1423" height="40" alt="image" src="https://github.com/user-attachments/assets/f8ec837a-ec0b-451e-acd9-36c8cea39da3" />
<img width="1452" height="166" alt="image" src="https://github.com/user-attachments/assets/204b7e57-a290-4f66-b4ba-8a1e870bdac5" />







