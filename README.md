# 🛒 Customer Shopping Behavior & Demographics Analysis

A dynamic end-to-end data analytics workflow and Power BI reporting dashboard designed to analyze retail customer purchasing habits, demographic revenue contributions, subscription tendencies, and product performance.

---

## Short Description / Purpose

The **Customer Shopping Behavior Dashboard** processes customer transaction records across 3,900 unique retail interactions to uncover key behavioral trends, product demand patterns, and customer segmentation metrics. This project demonstrates an end-to-end analytics pipeline—incorporating exploratory data analysis and feature engineering in Python (Jupyter Notebook), database migration and SQL analytical querying via MySQL, and interactive data visualization in Power BI.

---

## Tech Stack

The analysis and reporting ecosystem was built using the following technologies:

* 🐍 **Python & Pandas** – Primary data manipulation platform used for cleaning raw data, handling missing values via conditional imputation, transforming column schemes, and creating engineered features like `age_group` and `purchase_frequency_days`.
* 🛢️ **SQL & MySQL** – Database storage layer used for loading cleaned transactional tables and executing complex analytical SQL queries (incorporating CTEs, Window Functions, conditional aggregations, and CASE statements).
* 📊 **Power BI Desktop** – Core visual analytics platform used to build interactive report pages, dynamic measures, and key performance indicator (KPI) visual cards.
* 🧠 **DAX (Data Analysis Expressions)** – Used for calculated measures, dynamic aggregations, and filter context operations.
* 📁 **File Formats** – `.ipynb` for data preparation scripts, `.sql` for relational query execution, and `.pbix` for dashboard development.

---

## Data Source

The dataset contains transactional records of **3,900 customer interactions** encompassing 18 primary attributes prior to feature engineering.

* **Core Attributes:** `Customer ID`, `Age`, `Gender`, `Item Purchased`, `Category`, `Purchase Amount (USD)`, `Location`, `Size`, `Color`, `Season`, `Review Rating`, `Subscription Status`, `Shipping Type`, `Discount Applied`, `Previous Purchases`, `Payment Method`, and `Frequency of Purchases`.
* **Data Processing & ETL:** 
  * Imputed missing `Review Rating` values using category-level median aggregation.
  * Standardized column naming conventions and dropped redundant features (`promo_code_used` identified as duplicate to `discount_applied`).
  * Engineered binned feature `age_group` (Young Adult, Adult, Middle Aged, Senior) and mapped `purchase_frequency_days` for quantitative frequency modeling.

---

## Features / Highlights

### Business Problem
Retail companies struggle to identify which customer segments drive recurring revenue, how promotional discounts impact spend levels, and whether subscriber programs directly increase average order value. Answering questions such as:
* Do subscribed customers spend more than non-subscribers?
* Which age groups contribute the highest share of total revenue?
* How do discounts affect customer purchasing thresholds across various product categories?

...is difficult to achieve from unorganized raw transaction logs.

### Goal of the Dashboard
To deliver an end-to-end analytical solution that:
* Segments customers into actionable cohorts (**New**, **Returning**, and **Loyal**) based on historical purchase counts.
* Evaluates product performance and review ratings across distinct merchandise categories.
* Highlights revenue distribution by gender, age groups, shipping preferences, and subscription tier.

### Walkthrough of Key Visuals
* **Key Metrics & KPIs:** Total Customers (3,900), Average Purchase Amount ($59.76), Total Revenue generated, and overall Subscription adoption rate.
* **Revenue Contribution by Age Group (Bar Chart):** Ranks financial contributions across Young Adult, Adult, Middle Aged, and Senior segments.
* **Subscriber vs. Non-Subscriber Spend (Comparison Cards):** Directly contrasts total revenue and average spend between subscribed and standard users.
* **Top Products by Category & Rating (Stacked Bar / Matrix):** Breaks down top 3 items purchased within each category ranked by review scores and total order volume.
* **Discount Impact Analysis:** Evaluates discount penetration percentages across items and highlights high-spending discount users.
* **Customer Lifetime Segmentation (Pie / Donut Chart):** Visualizes the proportion of New (1 purchase), Returning (2–10 purchases), and Loyal (>10 purchases) buyers.

### Business Impact & Insights
* **Targeted Marketing:** Pinpoints high-value demographics to optimize promotional ad spending toward top revenue-generating age groups.
* **Subscription Program Optimization:** Assesses whether subscriber perks incentivize higher order values or simply encourage purchase frequency.
* **Inventory & Merchandising Strategy:** Identifies top-rated and most frequently purchased products per category to inform stock management and seasonal inventory planning.
