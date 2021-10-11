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

## Simple Selection of All Records

### Selecting All Data from a Table

Simple Select Statements

SQL = Structured Query Language
- Language used to talk to the database

15 Keywords will unlock a Database
- SELECT
- FROM
- WHERE
- AND
- OR
- BETWEEN
- IN
- DISTINCT
- ORDER BY
- DESC
- ASC
- LIMIT
- AS
- JOIN ON
- HAVING

Syntax that makes it easier to read
- Make the keywords like SELECT, FROM, WHERE all caps and names of fields and tables capitalize first letters of nouns/words

Syntax for selecting all data from Table

```sql
SELECT *
FROM <table_name>;
```

Go to northwind > Schemas > Query Tool

```sql
SELECT *
FROM customers;
```

```sql
SELECT *
FROM employees;
```

### Selecting Specific Fields

Use Field Names to Reduce Clutter

```sql
SELECT <column1>, <column2>, ...
FROM <table_name>;
```

```sql
SELECT companyname, city, country
FROM suppliers;
```

```sql
SELECT categoryname, description
FROM categories;
```

### Selecting Distinct Values

```sql
SELECT DISTINCT country
FROM customers;
```

```sql
SELECT DISTINCT city, country
FROM customers;
```

```sql
SELECT DISTINCT region
FROM suppliers;
```

### Counting Results

```sql
SELECT COUNT(*)
FROM Products;
```

```sql
SELECT COUNT(*)
FROM orders;
```

```sql
SELECT COUNT(DISTINCT city)
FROM  suppliers;
```

```sql
SELECT COUNT(DISTINCT productid)
FROM  order_details;
```

### Combining Fields in SELECT

```sql
SELECT orderid, shippeddate - orderdate AS duration
FROM orders;
```

```sql
SELECT orderid, unitprice * quantity AS orderprice
FROM order_details;
```

### Practice

1.- Select all fields, and all records from actor table

2.- Select all fields and records from film table

3.- Select all fields and records from the staff table

4.- Select address and district columns from address table

5.- Select title and description from film table

6.- Select city and country_id from city table

7.- Select all the distinct last names from customer table

8.- Select all the distinct first names from the actor table

9.- Select all the distinct inventory_id values from rental table

10.- Find the number of films ( COUNT ).

11.- Find the number of categories.

12.- Find the number of distinct first names in actor table

13.- Select rental_id and the difference between return_date and rental_date in rental table

```sql
--1
SELECT * FROM actor;

--2
SELECT * FROM film;

--3
SELECT * FROM staff;

--4
SELECT address,district FROM address;

--5
SELECT title,description FROM film;

--6
SELECT city,country_id FROM city;

--7
SELECT DISTINCT(last_name) FROM customer;

--8
SELECT DISTINCT(first_name) FROM actor;

--9
SELECT DISTINCT(inventory_id) FROM rental;

--10
SELECT COUNT(*) FROM film;

--11
SELECT COUNT(*) FROM category;

--12
SELECT COUNT(DISTINCT first_name) FROM actor;

--13
SELECT rental_id,return_date-rental_date FROM rental;
```












