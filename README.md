# Task 6: Sales Trend Analysis Using SQL

## 📄 Description

This project analyzes monthly sales trends from the *Sample - Superstore* dataset. It demonstrates how to extract and aggregate temporal data using SQL functions, and how to filter and sort results for insights into order volume and revenue.

## 🗃️ Dataset

- **Name:** Sample - Superstore
- **Format:** CSV
- **Loaded into Table:** `superstore`
- **Fields Used:** `order_date`, `sales`, `order_id`

## 🛠️ Steps Performed

1. **Create Table:**
   - Defined schema matching the CSV structure.

2. **Load Data:**
   - Imported CSV data using `LOAD DATA INFILE`.

3. **Analysis Query:**
   - Extracted **year** and **month** from `order_date`
   - Aggregated:
     - `SUM(sales)` as `total_revenue`
     - `COUNT(DISTINCT order_id)` as `order_volume`
   - Filtered for the year `2017`
   - Sorted by year and month
   - Limited results to **6 rows**

## 🧾 Sample Output

| year | month | total_revenue | order_volume |
|------|-------|----------------|---------------|
| 2017 | 1     | ...            | ...           |
| 2017 | 2     | ...            | ...           |
| ...  | ...   | ...            | ...           |

## 🧠 SQL Concepts Used

- `CREATE TABLE`
- `LOAD DATA INFILE`
- `EXTRACT(YEAR/MONTH FROM date)`
- `SUM()`, `COUNT(DISTINCT)`
- `GROUP BY`, `ORDER BY`, `LIMIT`
- `WHERE` clause with date filtering

## ✅ Requirements

- SQL engine that supports:
  - `EXTRACT()` function (e.g., MySQL, PostgreSQL)
  - `LOAD DATA INFILE` (ensure local file access is enabled)

## 📌 Note

- Modify the `LOAD DATA INFILE` path if needed for your environment.
- Adjust the `WHERE` clause to analyze different time periods.

