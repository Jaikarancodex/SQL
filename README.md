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

## Step 6: DROP TABLE 
Completely removes object (data + definition).After drop, it’s gone — you can’t select from it again unless recreated.
###
<img width="1423" height="40" alt="image" src="https://github.com/user-attachments/assets/f8ec837a-ec0b-451e-acd9-36c8cea39da3" />
<img width="1452" height="166" alt="image" src="https://github.com/user-attachments/assets/204b7e57-a290-4f66-b4ba-8a1e870bdac5" />

# DML (Data Manipulation Language)
### Commands that manipulate the data inside your tables -> INSERT, UPDATE, DELETE, SELECT
## INSERT — Add Data into the Table
<img width="1451" height="305" alt="image" src="https://github.com/user-attachments/assets/40f74cc6-8132-450b-8b63-9a77f588924d" />
<img width="1447" height="222" alt="image" src="https://github.com/user-attachments/assets/9fbe042c-4f1f-4552-9b56-aeacc94f15dc" />

## UPDATE — Modify Existing Data
### Eg: Fix a phone number
<img width="1441" height="207" alt="image" src="https://github.com/user-attachments/assets/4e8a243f-432c-42bb-8143-7217ad7f9d6d" />
<img width="1475" height="220" alt="image" src="https://github.com/user-attachments/assets/801e8295-2a7c-41f3-9125-1cdc8490e272" />

## DELETE — Remove Rows
### Remove a single employee
<img width="1453" height="188" alt="image" src="https://github.com/user-attachments/assets/3fc10291-22ad-4815-ab00-2118d6c7031e" />
<img width="1463" height="221" alt="image" src="https://github.com/user-attachments/assets/83f310c8-794e-4a7b-88bc-9e3cc51c6d68" />

# SELECT — Fetch / Read Data
This is where SQL shines. You can filter, sort, and analyze data easily.

## All rows
<img width="1463" height="221" alt="image" src="https://github.com/user-attachments/assets/ec97fe41-ba42-4e7a-b8e5-0bc5895ceca4" />

## Choose columns
<img width="1476" height="212" alt="image" src="https://github.com/user-attachments/assets/63d8433e-df69-4da2-8175-dc4bef3e55dd" />

## Filtering with WHERE
<img width="1478" height="191" alt="image" src="https://github.com/user-attachments/assets/369fe116-8943-4ec4-a03f-c18e6970f0d7" />

## Null checks
<img width="1470" height="163" alt="image" src="https://github.com/user-attachments/assets/93f1b21e-da03-4b1d-baea-9b0e36e9796c" />

## Pattern matching (LIKE)
<img width="1473" height="266" alt="image" src="https://github.com/user-attachments/assets/7e32470f-0cb8-4fcd-8619-7b51a946c5f6" />

## Sorting (ORDER BY)
<img width="1475" height="265" alt="image" src="https://github.com/user-attachments/assets/f295c7ce-6d17-4064-a726-1398444cecd0" />

# DCL (Data Control Language):
## GRANT: Assigning privileges to database users.

### Step 1:
##### Create a SQL Server login (server-level)
##### Switch to the target database and create a DB user mapped to that login
<img width="1452" height="285" alt="image" src="https://github.com/user-attachments/assets/184e290b-a93a-4197-867f-db7f3002d036" />

### Step 2:
on the Employees table and Still connected as admin, run:
###### //This allows intern_user to read rows from Employees.
###
<img width="1477" height="167" alt="image" src="https://github.com/user-attachments/assets/60ce7729-f601-4087-9240-6e4b95eb7ad5" />

### Step 3:
##### ->In SSMS, right-click on your server name in Object Explorer → choose Properties.
##### ->Go to Security (left panel).
##### ->Under Server authentication, select: SQL Server and Windows Authentication mode
##### ->Click OK.
##### ->Then restart the SQL Server service (important step): In SSMS: Right-click server name → Restart.
###### //This allows logins like intern_user to connect using passwords.
<img width="992" height="347" alt="image" src="https://github.com/user-attachments/assets/d5414ded-9e61-4ee9-adf9-c3a71be5d649" />

### Step 4:
##### File → Connect → Database Engine
##### Authentication: SQL Server Authentication
##### Login: intern_user
##### Password: Intern@123
##### (Server name stays the same as your main one — don’t change it)
###
<img width="800" height="500" alt="image" src="https://github.com/user-attachments/assets/355a496c-e859-4ef5-8464-3d61f0caa147" />

### Step 5:
Then open a new query window.
###
<img width="515" height="167" alt="image" src="https://github.com/user-attachments/assets/3e750947-a385-4712-a740-2c6d2449dc91" />

### Step 6:
In the new query window, run:
###
<img width="1477" height="185" alt="image" src="https://github.com/user-attachments/assets/66afddd7-d0af-4cb9-b12f-8ea93b8e6b84" />


## REVOKE: Revoking privileges from database users.
### Step 1:
Back in your admin connection, run this:
###
<img width="1452" height="183" alt="image" src="https://github.com/user-attachments/assets/1280b0b6-1e01-42d8-82a4-f05cf3eeaceb" />

### Step 2:
Then, go to your intern_user session and run:
###
<img width="1456" height="181" alt="image" src="https://github.com/user-attachments/assets/e466a56a-439a-4c4e-bde1-de7c807ff5ee" />

###### //"The SELECT permission was denied on the object 'Employees', database 'InternPractice', schema 'dbo'.” -> means your REVOKE worked!.



# DQL (Data Query Language): 
## SELECT (again): Retrieving data from one or more tables.  

# TCL (Transaction Control Language):
## COMMIT: Saving changes made during the current transaction. 
## ROLLBACK: Undoing changes made during the current transaction. 
## SAVEPOINT: Setting a point within a transaction to which you can later roll back. 

# Constraints: 
## PRIMARY KEY: Ensuring unique and not null values in a column. 
## FOREIGN KEY: Establishing a link between data in two tables. 
## UNIQUE: Ensuring unique values in a column or set of columns.  
## CHECK: Defining a condition that each row must satisfy. 
## NOT NULL: Ensuring a column cannot have a NULL value.      
















