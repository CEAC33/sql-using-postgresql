# sql-using-postgresql

## Intro

Why Learn SQL?
- Databases store all the world's information
- SQL is the standard way to talk to databases
- Almost any idea you can think of involves storing and retrieving data

What are databases?
- A place to store information

Main Types
- SQL Dtabases (this is what we are doing today)
- NoSQL Databases

Commercial SQL Databases
- Microsoft and Oracle are the dominant players

Open Source SQL Databases
- MySQL, MariaDB, PostgreSQL, SQLite

A Typical Database - Northwind
- Originally built as a demonstration database by Microsoft. It represents a company selling products from multiple suppliers to customers around the globe
- All Data is Grouped into Tables
- Each Table has 1 or more Fields
- Every Record is a Row in a Table

## Installing PostgreSQL and pgAdmin

https://www.postgresql.org/download/

### Install Northwind Database
- Run pgAdmin4
- Right Click PostgreSQL > Create > Database > northwind
- Download northwind.tar
- Right Click northwind > Restore
- If you have an error with the path, you can set it to `/Library/PostgreSQL/14/bin`
- Select the filename `northwind.tar`
- Go to Schemas > public > Tables > Refresh

### Install some Additional Databases
- Create 3 new databases called: usda, pagila and AdventureWorks.
- Load the usda.tar file into usda using the restore process covered in Lecture 3.
- Load the pagila.tar file into pagila using the same restore process.
- Load the AdventureWorks.tar file into AdventureWorks with restore as well.
