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

# Compared to the raw customer dataset, the following key transformations were performed:Name Consolidation: 

# Data Cleaning & Transformation Log (Customers Dataset)Name Consolidation:

-Combined first_name and last_name into a unified Full Name column for improved readability and user profile representation.

-Column Pruning & Cleanup: Removed the redundant customer_address column to streamline the schema, as higher-level regional analysis relies on city, state, and country.

-Locale-Based Date Formatting: Adjusted date field formats using Power Query's Using Locale option to standardise birthdate and acct_open_date into proper Date data types, resolving regional date-parsing inconsistencies.

-Value Standardisation: Replaced abbreviated categorical values with explicit, clear labels across key demographic attributes:Marital Status:

-Standardised M to Married and S to Single.Gender: Standardised F to Female and M to Male.

-Calculated Customer Age: Derived dynamic customer age (Customer_ages / Round Down) from the birthdate column to enable age-group segmentation.

-Conditional Membership Ranking: Created a custom conditional column (Member_card_ranking) to assign structured numerical hierarchy levels to customer loyalty tiers:Golden $\rightarrow 1$Silver $\rightarrow 2$Bronze $\rightarrow 3$Normal $\rightarrow 4$

# Data Cleaning & Transformation Log (Products Dataset)Currency Data Type Formatting:

-Converted product_retail_price and product_cost columns to explicit Currency / Decimal data types to enable accurate financial calculations (such as revenue and profit margins).

- Missing Value Imputation (Recyclable Attribute): Replaced null (NaN) values in the recyclable column with 0 (indicating non-recyclable items), establishing a standardized binary indicator ($1 = \text{Recyclable}$, $0 = \text{Non-Recyclable}$).

- Missing Value Imputation (Dietary Attribute): Replaced null (NaN) values in the low_fat column with 0 (indicating standard items), establishing a standardized binary indicator ($1 = \text{Low Fat}$, $0 = \text{Regular}$).

# Data Cleaning & Transformation Log (Stores & Transactions Datasets)

Date Format Detection & Standardization (Stores Dataset): Standardized date fields (first_opened_date and last_remodel_date) into explicit Date data types (M/D/YYYY) to ensure consistent temporal tracking for store aging and remodeling analysis.

Transaction Data Consolidation (Append Operation): Combined (appended) Transactions_1997 and Transactions_1998 into a single, master transaction fact table (Sales_Fact) 

Relational Merging & Feature Fetching:

Customer Profile Merge: Linked customer demographics from the Customers table to the merged transaction table using product_id.

Product Catalog Merge: Fetched pricing metadata (product_retail_price and product_cost) from the Products table into the transaction table using product_id.

Financial Metrics Calculation:

Selling Price (Total Revenue): Created a calculated field multiplying quantity by product_retail_price.

Cost Price (Total Cost): Created a calculated field multiplying quantity by product_cost.
## Analytics Scope & Business Use Cases:

-Revenue & Margin Analysis: Evaluating overall sales growth across 1997 vs. 1998, profit margins by product category, and high-performing store locations.
-Return Rate Optimization: Identifying products and store locations with disproportionately high return rates.
-Customer Segmentation: Analyzing spending trends across income brackets, loyalty card tiers (Bronze, Silver, Gold), and demographic groups.
-Store Footprint Performance: Measuring sales density (Revenue per Sq. Ft.) across store types and regions.
