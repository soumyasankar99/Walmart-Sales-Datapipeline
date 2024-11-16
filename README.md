# Walmart Sales Data Pipeline
![GitHub last commit](https://img.shields.io/github/last-commit/soumyasankar99/Walmart-Sales-Datapipeline)
![GitHub Repo stars](https://img.shields.io/github/stars/soumyasankar99/Walmart-Sales-Datapipeline?style=social)
![GitHub forks](https://img.shields.io/github/forks/soumyasankar99/Walmart-Sales-Datapipeline?style=social)


## Project Overview

![Walmart Sales Analysis Pipepline](https://github.com/user-attachments/assets/fa3f51ea-42eb-4e0f-85fa-cdc8028bd6f2)


This project demonstrates a data pipeline for analyzing Walmart sales and customer data using PySpark. Through the pipeline, we answer key business questions such as :

- total sales by state

- most purchased products ann monthly sales trends.

- The analysis is achieved by performing SQL-like transformations on large datasets, with results providing actionable insights.

## Technologies Used
![Walmart Sales Analysis Pipepline (1)](https://github.com/user-attachments/assets/8658f552-00a4-488b-bd3a-7dbd80c5cf69)


## Dataset
The project uses two tab-separated files:
1. **customers.tsv**: Contains customer details with columns `Customer Id`, `Name`, `City`, `State`, `Zip Code`.

2. **salestxns.tsv**: Contains sales transaction details with columns `Sales Txn Id`, `Category Id`, `Category Name`, `Product Id`, `Product Name`, `Price`, `Quantity`, `Customer Id`.

Dataset link: [Download Here][(https://docs.google.com/document/d/1b7UAYtTUZbXjuoGCQwsFHiBHBkM91Q8BFSPJ_zeIF6k/edit?tab=t.0)]

## Problem Statement
Using the PySpark framework, we answer the following questions:

1. **Total Number of Unique Customers**

2. **Total Sales by State**

3. **Top 10 Most Purchased Products**

4. **Average Transaction Value**

5. **Top 5 Customers by Expenditure**

6. **Product Purchases by a Specific Customer**

7. **Monthly Sales Trends**

8. **Category with Highest Sales**

9. **State-wise Sales Comparison**

10. **Detailed Customer Purchase Report**

## **Code Structure**

The project follows a modular structure with clearly defined functions for each step:

**Data Loading**: Loads customers.tsv and salestxns.tsv into PySpark DataFrames.

**Data Preprocessing**: Handles data type conversions and joins the data on Customer Id.

**Analysis Queries**: Answers each of the 10 questions with structured PySpark SQL queries.


## Insights and Results
Below are insights gained from each query:

1.**Total Number of Unique Customers:** Count of unique customers in the dataset.

2.**Total Sales by State:** Total revenue generated per state, highlighting top-performing states.

3.**Top 10 Most Purchased Products:** Products with the highest quantity sold, identifying popular items.

4.**Average Transaction Value:** Average sales value, providing insight into transaction trends.

5.**Top 5 Customers by Expenditure:** Customers who spent the most, useful for identifying VIP customers.

6.**Product Purchases by a Specific Customer:** List of products purchased by a selected customer, detailing their buying preferences.

7.**Monthly Sales Trends:** Sales per month to identify seasonal demand patterns.

8.**Category with Highest Sales:** Product category contributing the highest sales.

9.**State-wise Sales Comparison:** Comparison of sales between two specific states (e.g., Texas vs. Ohio).

10.**Detailed Customer Purchase Report:** Comprehensive report showing each customer’s purchases, transaction count, and average transaction value.    

## Project Setup 

### Prerequisites
- Python 3.7 or higher
- PySpark
- Java 8 or higher (required for PySpark)

#### Install dependencies: 

Use a virtual environment if desired, then install PySpark.
```
!pip install PySpark
```

# Project Documentation

> **📝 Note**  
> Ensure that the dataset files (customers.tsv and salestxns.tsv) are correctly placed in the specified paths.
> Any change in file location requires updating the paths in the code.
> Be aware of the exact column names in the TSV files. Names in the **Coustomer.tsv** and **salestxns.tsv** files might contain spaces or extra characters, so check and match them exactly.
  Convert columns like Price to float and Quantity to int for accurate calculations.


> **💡 Tip**  
> The join operation relies on matching Customer_Id between the DataFrames. Ensure that column names are identical after loading to avoid AnalysisException errors.

> **⚠️ Important**  
> PySpark requires a proper Java environment. Make sure Java is installed and accessible from your terminal before running PySpark.

> **🚨 Warning**  
> PySpark is case-sensitive. When referencing columns in queries, ensure names match exactly as in the DataFrame schema.

> **⚠️ Caution**  
> Large datasets can lead to high memory usage during group-by or join operations. Consider adjusting Spark’s memory settings or running the project on a cluster if your dataset is large.


### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/soumyasankar99/Walmart-Sales-Datapipeline.git
   cd walmart-sales-data-pipeline

