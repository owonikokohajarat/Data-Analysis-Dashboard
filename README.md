# Customer Segmentation using SQL
## Project Objective
The objective of your project is to use RFM (Recency, Frequency, Monetary) analysis to segment customers into meaningful groups, so that the business can make smarter, data‑driven decisions about retention, loyalty, and growth.

## Dataset Used
- <a href="https://www.kaggle.com/datasets/carrie1/ecommerce-data"> Dataset</a>

## Dataset Overview
•	Source: Retail transaction dataset
•	Period Covered: Up to December 2011
•	Key Fields: CustomerID, InvoiceNo, InvoiceDate, UnitPrice, Quantity
•	Preprocessing:
o	Cleaned missing values (e.g., replaced 'unknown' with NULL)
o	Standardized numeric fields (rounded UnitPrice to two decimals)
o	Ensured proper data types for dates and numeric columns

Chart Interaction - <a href="https://github.com/owonikokohajarat/Data-Analysis-Dashboard/blob/main/pareto_rfm_chart.png"> Dataset</a>

## Methodology
Step 1: Define Metrics
•	Recency: Days since last purchase relative to dataset cutoff date (2011-12-09).
•	Frequency: Number of distinct invoices per customer.
•	Monetary: Total spend per customer (UnitPrice × Quantity).

Step 2: SQL Implementation
A Common Table Expression (CTE) was used to calculate base metrics

Step 3: Adaptive Scoring with NTILE
To avoid manual thresholds, SQL’s NTILE(5) function was applied:
•	Recency: Lower values are better, reversed scoring.
•	Frequency: Higher values are better.
•	Monetary: Higher values are better.

Step 4: Segment Aggregation

Step 5: Visualization: 
Charts created in Python using Matplotlib and Seaborn.

## Dashboard
<img width="2390" height="790" alt="rfm_dashboard" src="https://github.com/user-attachments/assets/4dd0bd6e-c483-4396-8b84-ffeb5e5aa42d" />

