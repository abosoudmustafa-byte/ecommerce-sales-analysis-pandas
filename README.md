🛒 E-Commerce Sales Analysis
Data Cleaning & Time-Based Performance Insights
📌 Project Overview

This project analyzes an e-commerce transactions dataset using Python and Pandas.

The main objective is to:

Clean and validate raw transactional data

Transform line-level data into order-level insights

Perform time-based revenue analysis

Extract meaningful business insights

This project is part of my structured preparation for Machine Learning and Deep Learning.

🧠 Business Objective

Understand sales performance trends and customer purchasing behavior by answering:

How does revenue evolve over time?

Which months perform best and worst?

How stable is the Average Order Value (AOV)?

What is the impact of data cleaning on analysis accuracy?

📂 Dataset Structure

The dataset contains:

Order-level information (order_id, city, payment method, total)

Line-level product details (product_id, category, quantity, price)

Date and transaction metadata

A key challenge in this dataset was distinguishing between:

Line-level data (each row = product inside an order)

Order-level data (each order counted once)

This distinction was critical for accurate revenue calculations.

🧹 Data Cleaning Process

The dataset underwent multiple validation steps:

Removed rows with missing unit_price

Filled missing categorical values (city, payment_method)

Removed duplicated rows

Removed invalid quantities (quantity <= 0)

Converted order_date to datetime format

Created year and month features

A cleaned dataset was exported for reproducibility.

📊 Analytical Approach
1️⃣ Order-Level Aggregation

Converted line-level data into order-level data using:

groupby("order_id").first()

This prevented revenue double-counting.

2️⃣ Monthly Performance Analysis

Calculated:

Monthly Revenue

Monthly Orders

Monthly Average Order Value (AOV)

Used multi-column grouping:

groupby(["year", "month"])

to build time-based metrics.

📈 Monthly Revenue Trend


📊 Key Insights

Revenue shows a clear time-based trend across months.

Some months significantly outperform others.

Average Order Value remains relatively stable.

Data cleaning improved metric accuracy and removed inconsistencies.

Proper order-level aggregation prevented revenue inflation.

🛠 Technologies Used

Python

Pandas

NumPy

Matplotlib

Git & GitHub

📚 Skills Demonstrated

Data Cleaning & Validation

Multi-level GroupBy operations

Time-Series Aggregation

Feature Engineering

Analytical Thinking

Data Structuring (Line vs Order level)
