# Zomato-Dataset-Analysis-SQL
SQL analysis on the Zomato dataset to analyze user behavior and spending patterns.
# Zomato Dataset Analysis with SQL

## Overview
This project utilizes a sample dataset from Zomato, a popular restaurant discovery and food delivery platform, to perform SQL-based data analysis. The goal is to explore and query the Zomato dataset to extract meaningful insights. The project uses SQL queries to analyze data from various tables by joining them according to the requirements.

## Requirements
- SQL Database (e.g., MySQL Workbench)
- Zomato Dataset Tables (SQL scripts available in the repository)

## Database Setup
1. Create a new database in your SQL database management system.
2. Execute the provided SQL script (`zomato data files script.sql`) to create the necessary tables and insert data into the database.

## Files in this Repository
- **Zomato dataset analysis Questions Set.pdf**: A list of questions related to Zomato dataset analysis.
- **Zomato_dataset-Create Tables Query.txt**: The SQL queries to create the necessary tables in the database.
- **zomato analysis query and solution.docx**: SQL queries with solutions to analyze the Zomato dataset.
- **zomato data files script.sql**: SQL script file to create tables and insert data from the Zomato dataset.

## Sample Queries
Here are a few examples of queries used to analyze the dataset:

### How many days has each customer visited Zomato?
SELECT s.userid, SUM(p.price) AS total_expenditure
FROM sale AS s
LEFT JOIN product AS p ON s.product_id = p.product_id
GROUP BY s.userid
ORDER BY s.userid;


![image](https://github.com/user-attachments/assets/d6a392f0-4496-43fc-88a9-adef6a96fd07)
