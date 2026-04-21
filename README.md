# 📊 Telecom Customer Churn Analysis (Power BI Project)

## 📌 Project Overview
This project is a Power BI dashboard built to analyze customer churn behavior in a telecom company. The goal is to identify patterns and insights behind customer churn and help improve customer retention strategies through data-driven decision making.

---

## 📁 Dataset
The dataset used in this project contains telecom customer information, including:

- Customer demographics
- Account information
- Services subscribed
- Contract details
- Churn status (Yes/No)

---

## 🎯 Objectives
- Analyze customer churn rate
- Identify key factors influencing churn
- Understand customer behavior patterns
- Provide actionable insights for retention strategies

---

## 📊 Key Metrics (KPIs)
The dashboard includes the following key performance indicators:

- **Total Customers**  
  `Total Customers = COUNTROWS('telecom_churn')`

- **Churn Rate**
- **Total Churned Customers**
- **Active Customers**
- **Average Monthly Charges**
- **Total Revenue**

---

## 📈 Dashboard Features & Visuals

The Power BI report includes:

### 1. Overview Dashboard
- Total customers card
- Churn rate visualization
- Overall distribution of churn vs non-churn

### 2. Customer Demographics Analysis
- Gender distribution
- Senior citizen analysis
- Partner and dependents breakdown

### 3. Service Usage Analysis
- Internet service types
- Streaming services usage
- Phone service analysis

### 4. Contract & Payment Analysis
- Contract type vs churn
- Payment method distribution
- Monthly vs total charges comparison

### 5. Churn Insights
- Factors contributing to churn
- High-risk customer segments

---

## 🧹 Data Cleaning & Transformation (Power Query)
Before visualization, the dataset was cleaned and transformed:

- Removed null/blank values
- Converted **TotalCharges** to decimal format
- Standardized column data types
- Checked and corrected inconsistencies

---

## 🧮 DAX Measures Used
Some key DAX formulas used in this project:

```DAX
Total Customers = COUNTROWS('telecom_churn')

Total Churned Customers = CALCULATE(COUNTROWS('telecom_churn'), 'telecom_churn'[Churn] = "Yes")

Churn Rate = DIVIDE([Total Churned Customers], [Total Customers], 0)
