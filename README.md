# Task 7 – Basic Sales Summary with Python + SQLite

## What the code does
1. Creates a tiny SQLite DB (`sales_data.db`)
2. Inserts 6 sample sales rows
3. Runs one aggregation query  
   `GROUP BY product` calculating `total_qty` & `revenue`
4. Prints the DataFrame
5. Plots a revenue bar-chart (`sales_chart.png`)

## Key SQL
```sql
SELECT product,
       SUM(quantity)              AS total_qty,
       SUM(quantity * price)      AS revenue
FROM   sales
GROUP BY product
ORDER BY revenue DESC;
