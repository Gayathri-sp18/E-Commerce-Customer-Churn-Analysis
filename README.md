<div align="center">

# 🛒 E-Commerce Customer Churn Analysis

### MySQL | Customer Analytics | Data Exploration

<p>
  <img src="https://img.shields.io/badge/SQL-MySQL-blue?style=for-the-badge&logo=mysql&logoColor=white">
  <img src="https://img.shields.io/badge/Data%20Analysis-SQL-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Customer%20Analytics-Churn-green?style=for-the-badge">
</p>

</div>

---

## 📌 Project Overview

This project analyzes **e-commerce customer churn and customer behaviour using MySQL**.

The analysis explores customer demographics, purchasing behaviour, payment preferences, satisfaction, complaints, coupon usage, cashback, order activity, delivery distance, and customer returns.

The project demonstrates how SQL can be used to transform customer data into meaningful insights for understanding customer retention and churn patterns.

---

## 🎯 Objectives

* Analyze customer churn and retention patterns
* Explore customer purchasing behaviour
* Identify preferred payment methods and order categories
* Examine customer satisfaction and complaints
* Analyze coupon and cashback usage
* Compare customer activity across city tiers
* Categorize customers based on warehouse-to-home distance
* Analyze the relationship between returns, complaints, and churn
* Extract business insights using SQL

---

## 🗂️ Dataset

The primary dataset contains customer-level information covering:

* Customer tenure
* Preferred login device
* City tier
* Warehouse-to-home distance
* Preferred payment mode
* Gender
* App usage
* Registered devices
* Preferred order category
* Satisfaction score
* Marital status
* Number of addresses
* Order amount growth
* Coupon usage
* Order count
* Days since last order
* Cashback amount
* Complaints
* Churn status

A separate Customer Returns table is also created to analyze return activity alongside customer churn and complaints.

---

## 🔍 Analysis Performed

### 👥 Customer Churn

* Active vs. churned customer distribution
* Average tenure of churned customers
* Total cashback received by churned customers
* Complaint percentage among churned customers

### 🛍️ Customer Behaviour

* Preferred order categories
* Order activity by customer segment
* Coupon usage patterns
* Customer activity across city tiers

### 💳 Payment Analysis

* Most preferred payment method among active customers
* Device usage among UPI customers
* Payment preferences under specific customer conditions

### ⭐ Satisfaction & Complaints

* Maximum satisfaction score
* Average satisfaction score among customers who complained
* Order activity of highly satisfied customers

### 💰 Cashback & Coupons

* Average cashback by order category
* Top categories based on average cashback
* Order categories associated with higher coupon usage

### 📍 Distance & Churn

Customers are categorized into:

`Very Close` → `Close` → `Moderate` → `Far`

The analysis compares these distance categories with customer churn status.

### 🔄 Customer Returns

A separate returns dataset is connected with customer information using an `INNER JOIN` to identify returned customers who are both churned and complaint-affected.

---

## 🧠 SQL Concepts Used

<div align="center">

`SELECT` · `WHERE` · `GROUP BY` · `ORDER BY` · `LIMIT` · `DISTINCT`

`CASE` · `COUNT()` · `SUM()` · `AVG()` · `MAX()` · `ROUND()`

`UPDATE` · `ALTER TABLE` · `CREATE TABLE` · `INSERT INTO`

`INNER JOIN` · `Subqueries` · `Conditional Aggregation`

</div>

---

## 📊 Key Analytical Areas

| Area                   | Analysis                       |
| ---------------------- | ------------------------------ |
| **Churn**              | Active vs. churned customers   |
| **Customer Behaviour** | Orders, categories & app usage |
| **Payments**           | Preferred payment methods      |
| **Satisfaction**       | Satisfaction & complaints      |
| **Marketing**          | Coupons & cashback             |
| **Location**           | City tier & delivery distance  |
| **Returns**            | Returns, complaints & churn    |

---

## 🛠️ Tools & Technologies

**Database:** MySQL
**Environment:** MySQL Workbench
**Analysis:** SQL
**Version Control:** GitHub

---

## 💼 Skills Demonstrated

* SQL Data Analysis
* Data Exploration
* Data Cleaning & Transformation
* Customer Churn Analysis
* Aggregation & Filtering
* Joins & Subqueries
* Conditional Logic
* Business Problem Solving
* Customer Behaviour Analysis

---

## 📁 Project Structure

```text
E-Commerce-Customer-Churn-Analysis/
│
├── E-Commerce_Customer_Churn_Analysis.sql
└── README.md
```

---



### 👩‍💻 Gayathri S Pillai

**Aspiring Data Analyst | MBA – Business Analytics & Marketing**

<div align="center">

⭐ *Turning data into meaningful business insights.*

</div>
