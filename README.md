# sql-stat-olist-analysis-
Basic statistical analysis of the Olist database using MySQL(percentages, expected value, distribution functions, breakdown by category)
# Olist E-commerce Analysis (MySQL)

A SQL project on the public Brazilian marketplace dataset by Olist: ~100K orders from 2016-2018. The goal is to create a tool for answering questions  about sales, delivery, and order cancellations.

**Tools:** MySQL 8.0, MySQL Workbench
**Data:** [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle)

## Repository Structure

- `schema_olist.sql`: table definitions
- `stat_analysis.zip`: analytical queries, one business question per file

## Tables

| Table | Description |
|---|---|
| `orders` | orders, statuses, timestamps |
| `order_items` | items in each order, price, freight cost |
| `customers` | customers and their state |
| `order_payments` | payments per order |
| `products` | products and their categories |
| `category_translation` | category names translated to English |

## How to Reproduce

1. Download the dataset from Kaggle (link above).
2. Run `schema_olist.sql`.
3. Import the CSV files into the matching tables (`LOAD DATA INFILE`).
4. Run the queries from the `stat_analysis.zip` folder.

## Questions

| File | Question |
|---|---|
| `delay_pntg.sql` | What share of orders was canceled each month? |
| `delay_prb.sql` | What share of orders was delivered late, and how does it vary by customer state? |
| `edf_cost.sql` | What is the empirical distribution of order values, and what proportion of orders cost up to 50, 100, and 200? |
| `EV.sql` | What are the mean, median, and standard deviation of order values by month?? |
| `orders_distribution.sql` | How are orders distributed by the number of items they contain (1, 2, 3, or 4 and more)? |
| `season.sql` | How did monthly sales revenue change over time, and what was the month-over-month growth rate? |

