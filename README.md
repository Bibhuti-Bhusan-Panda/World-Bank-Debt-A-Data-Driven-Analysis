# World Bank International Debt Analysis

![SQL](https://img.shields.io/badge/Language-SQL-blue.svg)
![Database](https://img.shields.io/badge/Database-PostgreSQL-orange.svg)
![Project](https://img.shields.io/badge/Project-Data_Analysis-green.svg)

This project provides a comprehensive SQL-based analysis of international debt data from The World Bank. The primary objective is to query a detailed dataset to extract meaningful insights about the debt owed by developing countries across various economic indicators.

## Table of Contents
- [About the Dataset](#about-the-dataset)
- [Project Setup](#project-setup)
- [Analysis and Key Findings](#analysis-and-key-findings)
- [Tools Used](#tools-used)
- [Conclusion](#conclusion)

## About the Dataset

The dataset is sourced from The World Bank and contains records of debt owed by various countries.

* *Source*: The World Bank
* *Content*: The data details long-term external debt for developing countries, broken down by various creditor types and repayment metrics.
* *File*: Debt Dataset.csv

### Dataset Schema
The international_debt table has the following structure:
| Column | Data Type | Description |
|---|---|---|
| country_name | varchar(50) | The name of the country. |
| country_code | varchar(50) | The unique 3-letter ISO code for the country. |
| indicator_name| text | A descriptive name for the debt indicator. |
| indicator_code| text | A unique code for the debt indicator. |
| debt | numeric | The amount of debt in current US dollars. |


## Project Setup

To replicate this analysis, you will need a SQL database system (e.g., PostgreSQL, MySQL).

1.  *Create the Database*: Set up a new database named International_Debt.

2.  *Create the Table*: Use the following SQL command to create the international_debt table:
    sql
    CREATE TABLE international_debt
    (
      country_name varchar(50),
      country_code varchar(50),
      indicator_name text,
      indicator_code text,
      debt numeric
    );
    

3.  *Import Data*: Import the data from the Debt Dataset.csv file into the newly created table.

## Analysis and Key Findings

A series of SQL queries were executed to explore the data and answer critical questions about global debt.

### 1. How many distinct countries are in the dataset?
The analysis identified a total of *124* distinct countries in the dataset.

### 2. What is the total amount of debt owed by these countries?
The combined debt of all countries across all indicators is approximately *$3.08 trillion USD*.

### 3. Which country has the highest total debt?
*China* holds the highest aggregate debt in the dataset. The top 5 countries by total debt are:
1.  China
2.  Brazil
3.  India
4.  South Asia
5.  Russian Federation

### 4. What is the average debt amount across different debt categories?
The analysis shows that the "Principal repayments on external debt, long-term (AMT, current US$)" indicator has the highest average debt value, indicating large repayment sums across countries.

### 5. What is the highest principal repayment amount?
The highest single record for principal repayments belongs to *China* for the indicator "Principal repayments on external debt, long-term (AMT, current US$)".

### 6. What are the most common debt indicators?
The most frequently occurring indicators in the dataset relate to principal repayments, interest payments, and disbursements from various creditor types (bilateral, multilateral, etc.). This suggests the data is comprehensive in tracking the full lifecycle of debt.

## Tools Used
* *SQL*: The primary language used for data querying, aggregation, and analysis.

## Conclusion
This project successfully demonstrates the power of SQL for conducting in-depth financial data analysis. By querying the World Bank's debt dataset, we were able to extract high-level summaries and specific, granular insights, painting a clearer picture of the international debt landscape for developing nations.
