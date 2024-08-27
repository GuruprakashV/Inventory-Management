# Inventory-Management
An SQL-based inventory management system database for handling products, categories, suppliers, and orders. Includes sample data and queries to manage and analyze inventory effectively.
Overview
The InventoryManagement database is designed to manage inventory for a business, including products, categories, suppliers, orders, and order details. The database schema includes tables for Categories, Products, Suppliers, Orders, and OrderDetails, with constraints and relationships to maintain data integrity.

Database Schema
Tables
Categories

Fields:
category_id (INT): Primary Key, Auto-incremented.
category_name (VARCHAR 100): Unique, Not Null.
description (TEXT).
Products

Fields:
product_id (INT): Primary Key, Auto-incremented.
product_name (VARCHAR 100): Not Null.
category_id (INT): Foreign Key referencing Categories(category_id).
price (DECIMAL 10, 2): Not Null.
stock_quantity (INT): Not Null.
reorder_level (INT): Not Null.
Suppliers

Fields:
supplier_id (INT): Primary Key, Auto-incremented.
supplier_name (VARCHAR 100): Not Null.
contact_name (VARCHAR 50).
address (TEXT).
phone_number (VARCHAR 15): Unique.
Orders

Fields:
order_id (INT): Primary Key, Auto-incremented.
order_date (DATE): Not Null.
supplier_id (INT): Foreign Key referencing Suppliers(supplier_id).
total_amount (DECIMAL 10, 2): Not Null.
OrderDetails

Fields:
order_detail_id (INT): Primary Key, Auto-incremented.
order_id (INT): Foreign Key referencing Orders(order_id).
product_id (INT): Foreign Key referencing Products(product_id).
quantity (INT): Not Null.
unit_price (DECIMAL 10, 2): Not Null.

Data Insertion
Sample data has been inserted into the Categories, Suppliers, Products, Orders, and OrderDetails tables to illustrate how the database functions. This data can be used to run queries and test the database structure.

SQL Queries
A set of SQL queries has been provided to perform various operations, such as:


1.	Retrieve the names and prices of all products that are currently out of stock.
2.	List the total number of products in each category.
3.	Find all suppliers who have supplied products worth more than $10,000.
4.	Get the details of products with a stock quantity less than their reorder level.
5.	Retrieve the order IDs and total amounts for orders placed in the last 30 days.
6.	List all products along with their categories, ordered by product name.
7.	Get the names of suppliers who have not supplied any products in the last 6 months.
8.	Find the total amount spent on orders for each supplier.
9.	Retrieve the product names and total quantities ordered for each product in the last year.
10.	Get a list of products that belong to the Electronics category and have a price greater than $500.
