# Zepto E-commerce SQL Data Analysis Project

## Overview
This project is a SQL-based data analysis of an e-commerce inventory dataset from Zepto. It was completed as a personal portfolio project to practice working with real-world retail data using PostgreSQL and to demonstrate analytical thinking through SQL.

The analysis focuses on understanding product pricing, discounts, stock availability, and inventory distribution using structured queries.

---

## Dataset Description
The dataset represents product inventory data scraped from Zepto’s platform and sourced from Kaggle. Each record corresponds to a unique Stock Keeping Unit (SKU). Duplicate product names exist because the same product can appear in multiple package sizes, weights, pricing, or discount variations, which reflects real-world e-commerce catalog behavior.

**Dataset Source:**  
https://www.kaggle.com/datasets/palvinder2006/zepto-inventory-dataset

### Columns
- **sku_id**: Unique identifier for each SKU  
- **name**: Product name  
- **category**: Product category  
- **mrp**: Maximum Retail Price (converted from paise to INR)  
- **discountPercent**: Discount applied on MRP  
- **discountedSellingPrice**: Final selling price after discount (INR)  
- **availableQuantity**: Units available in inventory  
- **weightInGms**: Product weight in grams  
- **outOfStock**: Boolean flag indicating stock availability  
- **quantity**: Units per package  

---

## Tools Used
- PostgreSQL  
- pgAdmin 4  
- SQL  

---

## Analysis Workflow

### 1. Database and Table Creation
A relational table was created in PostgreSQL with appropriate data types to store the inventory data.

### 2. Data Import
The dataset was imported using pgAdmin’s CSV import functionality. Encoding issues were resolved by converting the file to UTF-8 format prior to import.

### 3. Data Exploration
Initial exploration was performed to:
- Count the total number of records  
- Review sample data  
- Identify null values  
- Analyze distinct product categories  
- Compare in-stock and out-of-stock products  
- Detect duplicate product names across multiple SKUs  

### 4. Data Cleaning
Data quality issues were addressed by:
- Removing records with invalid pricing (MRP equal to zero)  
- Converting pricing fields from paise to rupees for consistency  

### 5. Business Analysis
SQL queries were written to answer business-focused questions, including:
- Identifying top products based on discount percentage  
- Finding high-MRP products that are out of stock  
- Estimating potential revenue by product category  
- Filtering high-priced products with low discounts  
- Ranking categories by average discount percentage  
- Calculating price per gram to assess value for money  
- Grouping products based on weight categories  
- Computing total inventory weight by category  

---

## Repository Structure

The `zepto_queries.sql` file contains all SQL statements used for table creation, data exploration, data cleaning, and analysis.

---

## How to Run
1. Create a PostgreSQL database  
2. Open pgAdmin and connect to the database  
3. Load the `zepto_queries.sql` file in the Query Tool  
4. Execute the queries to reproduce the analysis  

---

## Notes
This project was completed for personal learning and portfolio purposes and focuses on applying SQL to realistic business problems using retail inventory data.

---

## Author
Developed as an individual data analysis project using PostgreSQL.

