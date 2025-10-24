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
<img width="1541" height="166" alt="Screenshot 2025-10-23 234125" src="https://github.com/user-attachments/assets/902a7494-470a-4aeb-acf3-fc5c23042a34" />

## Aggregating data using functions like COUNT, SUM, AVG, MIN, MAX. 
<img width="1541" height="166" alt="Screenshot 2025-10-23 234125" src="https://github.com/user-attachments/assets/902a7494-470a-4aeb-acf3-fc5c23042a34" />
<img width="1540" height="279" alt="Screenshot 2025-10-23 234042" src="https://github.com/user-attachments/assets/0a76fb10-30d8-48fe-ada8-e2b716bb1c40" />

## Grouping data with GROUP BY. 
<img width="1627" height="251" alt="image" src="https://github.com/user-attachments/assets/2180f438-7047-494b-a789-74a59d265076" />

## Sorting results with ORDER BY. 
<img width="1537" height="279" alt="Screenshot 2025-10-23 235828" src="https://github.com/user-attachments/assets/76507963-0a49-4a9b-94d4-58f4fb2cba23" />

## Filtering aggregated data with HAVING. 
<img width="1623" height="236" alt="image" src="https://github.com/user-attachments/assets/2ba8298e-9655-41e5-bcaa-11f79c8f2ec6" />

# TCL (Transaction Control Language):
## COMMIT: Saving changes made during the current transaction. 
BEGIN TRANSACTION starts a “temporary change area.” -> You updated a row. -> COMMIT saves it permanently.
###
<img width="1586" height="301" alt="image" src="https://github.com/user-attachments/assets/1de71e04-0946-4db5-a2bd-cdc48dc93534" />

##### If you check:
<img width="1622" height="160" alt="image" src="https://github.com/user-attachments/assets/e77e9102-867c-43b1-870c-831a7da060af" />

###### //You’ll see Karan’s salary increased — permanently.

## SAVEPOINT: Setting a point within a transaction to which you can later roll back.
Sometimes you want to undo some changes, not all. That’s where SAVEPOINT comes in.
###
<img width="1622" height="347" alt="image" src="https://github.com/user-attachments/assets/529b4993-4865-422b-9ffe-d14fd8fc6cf4" />

##### Now Karan's and Aegon's salary were updated and saved as SAVEPOINT.
<img width="1626" height="202" alt="image" src="https://github.com/user-attachments/assets/5c5f4de8-3e1a-4c22-80f0-fee1096a91aa" />

## ROLLBACK: Undoing changes made during the current transaction. 
##### ->The change happens temporarily.  
##### ->ROLLBACK cancels it — like Ctrl+Z for your database. 
##### ->The salary stays the same as before.
<img width="1623" height="165" alt="image" src="https://github.com/user-attachments/assets/3041fdff-879a-412a-851b-b8b1d6e776cd" />

##### Now Aegon’s change is undone. Because we saved his update as sp2: -> undo everything after sp1
<img width="1630" height="197" alt="image" src="https://github.com/user-attachments/assets/2eaf6c7d-299f-458b-9aaa-23823b26483e" />

##### COMMIT finalizes everything before sp1.
<img width="1617" height="141" alt="image" src="https://github.com/user-attachments/assets/61bb4dd2-62ff-4a51-9a8a-ac58063d2947" />


# Constraints: 
## PRIMARY KEY: Ensuring unique and not null values in a column. 
## FOREIGN KEY: Establishing a link between data in two tables. 
## UNIQUE: Ensuring unique values in a column or set of columns.  
## CHECK: Defining a condition that each row must satisfy. 
## NOT NULL: Ensuring a column cannot have a NULL value.      
















