# Customer Churn Analysis

## Project Overview

This project is an end-to-end Customer Churn Analysis using SQL Server, Python, and Power BI.

The objective of the project is to identify customer churn patterns, understand the factors associated with customers leaving, and provide business recommendations that can help improve customer retention.

---

## Tools & Technologies

- SQL Server / SSMS
- Python
- Pandas
- NumPy
- Matplotlib
- Power BI
- DAX
- Power Query
- Excel
- GitHub

---

## Business Objectives

The analysis focuses on answering questions such as:

- What is the overall customer churn rate?
- How many customers have churned?
- Which customer groups have the highest churn rate?
- Does customer tenure affect churn?
- Does contract type influence churn?
- Are customers with higher monthly charges more likely to churn?
- Which payment methods have higher churn rates?
- Does internet service type affect churn?
- Which customer segments should the company prioritize for retention?

---

## Project Workflow

Dataset
↓
Data Cleaning
↓
Python EDA
↓
SQL Analysis
↓
Data Modeling
↓
Power BI Dashboard
↓
Business Insights
↓
Recommendations

---

## Data Cleaning

The dataset was prepared and cleaned before analysis.

Key cleaning activities included:

- Checking missing values
- Removing duplicate records
- Correcting data types
- Standardizing categorical values
- Validating customer IDs
- Cleaning Total Charges and Monthly Charges
- Preparing churn indicators
- Creating tenure groups

---

## SQL Analysis

SQL Server was used to perform customer-level analysis including:

- Total Customers
- Total Churned Customers
- Overall Churn Rate
- Churn by Gender
- Churn by Contract Type
- Churn by Internet Service
- Churn by Payment Method
- Churn by Tenure
- Churn by Monthly Charges
- Customer Revenue Analysis
- High-Risk Customer Segments

---

## Python EDA

Python was used for exploratory data analysis and data validation.

Libraries used:

- Pandas
- NumPy
- Matplotlib

Analysis included:

- Churn distribution
- Customer tenure analysis
- Monthly charges analysis
- Contract analysis
- Payment method analysis
- Internet service analysis
- Customer demographic analysis

---

## Data Model

A star-schema-style model was created for Power BI.

### Fact Table

`FactCustomer`

Important fields include:

- CustomerID
- ContractID
- InternetServiceID
- PaymentMethodID
- Tenure
- MonthlyCharges
- TotalCharges
- Churn

### Dimension Tables

- DimCustomer
- DimContract
- DimInternetService
- DimPaymentMethod

---

## Power BI Dashboard

The Power BI dashboard provides an interactive view of customer churn.

### KPI Cards

- Total Customers
- Churned Customers
- Active Customers
- Churn Rate
- Average Monthly Charges
- Average Tenure

### Dashboard Visuals

- Churn Rate by Tenure Group
- Churn by Contract Type
- Churn by Internet Service
- Churn by Payment Method
- Churn by Gender
- Monthly Charges: Churned vs Stayed
- Customer Distribution
- Revenue Analysis

### Filters / Slicers

- Contract Type
- Internet Service
- Payment Method
- Gender
- Tenure Group

---

## Important DAX Measures

Examples of measures used in the dashboard:

### Total Customers

```DAX
Total Customers =
DISTINCTCOUNT(FactCustomer[CustomerID])
