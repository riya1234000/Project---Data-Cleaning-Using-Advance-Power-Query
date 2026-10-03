# Project---Data-Cleaning-Using-Advance-Power-Query

## Retail Customer & Sales Data Cleaning Project


##  Project Overview
This project focuses on cleaning, transforming, and modeling a multi-table retail dataset using Excel (Power Query). The raw data contained inconsistent formatting, missing values, unformatted fields, and transactional data split across multiple years.

The goal of this project was to perform comprehensive Data Preprocessing, Feature Engineering, and Data Integration to prepare a clean, analytics-ready dataset for downstream reporting and dashboarding.

## Datasets
##  Customers (Customers.csv)
 <a href="https://github.com/riya1234000/Project---Data-Cleaning-Using-Advance-Power-Query/blob/main/Customers.csv">Dataset</a>

## Products (Products.csv)
<a href="https://github.com/riya1234000/Project---Data-Cleaning-Using-Advance-Power-Query/blob/main/Products.csv">Dataset</a>

## Regions (Regions.csv)
<a href="https://github.com/riya1234000/Project---Data-Cleaning-Using-Advance-Power-Query/blob/main/Regions.csv">Dataset</a>

## Returns_1997-1998 (Returns_1997-1998.csv)
<a href="https://github.com/riya1234000/Project---Data-Cleaning-Using-Advance-Power-Query/blob/main/Returns_1997-1998.csv">Dataset</a>

## Stores (Stores.csv)
<a href="https://github.com/riya1234000/Project---Data-Cleaning-Using-Advance-Power-Query/blob/main/Stores.csv">Dataset</a>

## Transactions_1997 (Transactions_1997.csv)
<a href="https://github.com/riya1234000/Project---Data-Cleaning-Using-Advance-Power-Query/blob/main/Transactions_1997.csv">Dataset</a>

## Transactions_1998 (Transactions_1998.csv)
<a href="https://github.com/riya1234000/Project---Data-Cleaning-Using-Advance-Power-Query/blob/main/Transactions_1998.csv">Dataset</a>

## Preprocessing & Data Cleaning Summary

- Here are the data cleaning steps performed during the Power Query preparation phase:
- Table Unioning & Append: Appended Transactions_1997 and Transactions_1998 into a single, consolidated Sales_Fact table with 269,720 total transactions.
- Text Standardization: Cleaned extra spaces using TRIM and standardized character casing across customer names, product categories, and store location text fields.
- Data Type Correction: Updated data types to explicit formats—setting transaction dates to Date, purchase quantities to Whole Number, and monetary fields (product_retail_price, product_cost) to Currency/Decimal.
- Handling Nulls & Anomalies: Filled missing values in customer demographic fields with explicit placeholders (Unspecified/CUST_GUEST) to maintain relational and foreign key integrity.
- Calculated Helper Attributes: Created custom calculated columns for total financial metrics
- Total Revenue: $\text{Quantity} \times \text{Retail Price}$Total Cost: $\text{Quantity} \times \text{Cost}$

## Analytics Scope & Business Use Cases:

-Revenue & Margin Analysis: Evaluating overall sales growth across 1997 vs. 1998, profit margins by product category, and high-performing store locations.
-Return Rate Optimization: Identifying products and store locations with disproportionately high return rates.
-Customer Segmentation: Analyzing spending trends across income brackets, loyalty card tiers (Bronze, Silver, Gold), and demographic groups.
-Store Footprint Performance: Measuring sales density (Revenue per Sq. Ft.) across store types and regions.
