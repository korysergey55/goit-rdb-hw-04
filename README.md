# goit-rdb-hw-04 Relational Databases 

Tasks:

1. Create a database to manage the book library according to the structure given below. Use DDL commands to create the necessary tables and their relationships.
Database structure

a) Scheme name — “LibraryManagement”

b) "authors" table:
author_id (INT, auto-increment PRIMARY KEY)
author_name (VARCHAR)

c) Table "genres":
genre_id (INT, auto-increment PRIMARY KEY)
genre_name (VARCHAR)

d) Table "books":
book_id (INT, auto-increment PRIMARY KEY)
title (VARCHAR)
publication_year (YEAR)
author_id (INT, FOREIGN KEY relation to "Authors")
genre_id (INT, FOREIGN KEY relation to "Genres")

e) Table "users":
user_id (INT, auto-increment PRIMARY KEY)
username (VARCHAR)
email (VARCHAR)

f) Table "borrowed_books":
borrow_id (INT, auto-increment PRIMARY KEY)
book_id (INT, FOREIGN KEY relation to "Books")
user_id (INT, FOREIGN KEY relation to "Users")
borrow_date (DATE)
return_date (DATE)

2. Fill in the tables with simple fictitious test data. One or two rows in each table are enough.

3. Go to the database that you worked with in topic 3. Write a query using the FROM and INNER JOIN statements that joins all the data tables that we loaded from the files: order_details, orders, customers, products, categories, employees, shippers, suppliers. To do this, you need to find shared keys. Check the correct execution of the request.

4. Follow the prompts listed below.
- Determine how many rows you got (using the COUNT statement).
- Change several INNER statements to LEFT or RIGHT. Determine what happens to the number of rows. Why? Write the answer in a text file.
- Select only those rows where employee_id > 3 and ≤ 10.
- Group by category name, count number of rows in group, average product quantity (product quantity is in order_details.quantity)
- Filter out rows where the average number of items is greater than 21.
- Sort the rows in descending order of number of rows.
- Display (select) four lines with the first line omitted.