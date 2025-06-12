# TASK7-SQLITE-Database

The project that connects Python to a tiny SQLite database, runs simple SQL queries, and visualizes basic sales insights using Pandas and Matplotlib.

🔧 Tools & Technologies
Python 3.x

SQLite (built-in via sqlite3)

Jupyter Notebook or .py script

Pandas

Matplotlib

📁 Project Overview
This project demonstrates how to:

Connect Python to a SQLite database

Run SQL queries using Python

Calculate total quantity and revenue by product

Visualize the results using a bar chart

📦 Dataset
We create a small sales_data.db file with one table:

sql
CREATE TABLE sales (
  product TEXT,
  quantity INTEGER,
  price REAL
);


Sample records:

text
("Product A", 5, 10.0)  
("Product B", 3, 15.0)  
("Product A", 2, 10.0)  
("Product C", 7, 20.0)


🧠 SQL Logic
We group and summarize data:

sql
SELECT product,
       SUM(quantity) AS total_qty,
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;


📈 Output
A DataFrame showing each product’s total quantity and revenue

A Matplotlib bar chart: "Sales Revenue by Product"

Chart saved as sales_chart.png

