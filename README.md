# 🛒 E-Commerce Customer Churn Analysis — MySQL

<p align="center">
  <b>Customer Churn Analysis using MySQL</b><br>
  Data Cleaning • SQL Queries • Customer Behaviour Analysis • Business Insights
</p>

---

## 📌 Project Overview

This project focuses on analyzing **e-commerce customer churn and customer behaviour using MySQL**.

The dataset contains customer-level information such as tenure, login device, payment mode, order category, satisfaction score, complaints, coupon usage, order count, cashback amount, and churn status.

The project involves creating a MySQL database, preparing and transforming the customer data, performing exploratory analysis, and answering business-oriented questions using SQL.

The analysis also includes a separate Customer Returns table to examine relationships between returns, customer complaints, and churn status.

---

## 🎯 Objectives

The main objectives of this project are to:

* Analyze customer churn patterns.
* Understand customer behaviour and purchasing preferences.
* Examine customer satisfaction and complaints.
* Analyze payment methods and order categories.
* Explore coupon and cashback usage.
* Compare customer activity across different city tiers.
* Categorize customers based on warehouse-to-home distance.
* Identify relationships between customer returns, complaints, and churn.
* Generate meaningful insights using SQL queries.

---

## 🗃️ Database & Tables

### Database

```sql
ecomm
```

### Main Table

```text
customer_churn
```

The `customer_churn` table contains customer-level behavioural and demographic information, including:

| Column                      | Description                                          |
| --------------------------- | ---------------------------------------------------- |
| CustomerID                  | Unique customer identifier                           |
| Churn                       | Original churn indicator                             |
| Tenure                      | Customer tenure                                      |
| PreferredLoginDevice        | Preferred device used to log in                      |
| CityTier                    | Customer city classification                         |
| WarehouseToHome             | Distance between warehouse and home                  |
| PreferredPaymentMode        | Preferred payment method                             |
| Gender                      | Customer gender                                      |
| HourSpendOnApp              | Time spent on the application                        |
| NumberOfDeviceRegistered    | Number of registered devices                         |
| PreferedOrderCat            | Preferred order category                             |
| SatisfactionScore           | Customer satisfaction rating                         |
| MaritalStatus               | Customer marital status                              |
| NumberOfAddress             | Number of registered addresses                       |
| Complain                    | Original complaint indicator                         |
| OrderAmountHikeFromlastYear | Increase in order amount compared with previous year |
| CouponUsed                  | Number of coupons used                               |
| OrderCount                  | Number of orders                                     |
| DaySinceLastOrder           | Days since the customer's last order                 |
| CashbackAmount              | Cashback received                                    |

The project later creates more descriptive fields such as:

* `ComplaintReceived`
* `ChurnStatus`

These are used to make the analysis easier to interpret.

---

## 🔄 Data Preparation & Transformation

The SQL workflow includes several data preparation and transformation steps before analysis.

### Key transformations include:

* Creating the `ecomm` database.
* Creating the `customer_churn` table.
* Loading customer records into the database.
* Handling missing values during analysis.
* Creating a readable complaint status.
* Creating a readable churn status.
* Removing the original binary `Churn` and `Complain` columns after creating descriptive status fields.
* Creating a separate `customer_returns` table.
* Combining customer and return information using an `INNER JOIN`.

For example, churn is transformed into a more readable status:

```sql
CASE
    WHEN Churn = 1 THEN 'Churned'
    ELSE 'Active'
END
```

The resulting values are stored in the `ChurnStatus` column.

---

## 🔍 Analysis Performed

The project answers multiple business questions using SQL.

### 👥 Customer Churn

* Count of active and churned customers.
* Average tenure of churned customers.
* Total cashback received by churned customers.
* Percentage of churned customers who submitted complaints.

### 🛍️ Customer Purchasing Behaviour

* Most common order categories.
* Customer distribution across city tiers.
* Total order amount increase for selected customer groups.
* Average order count.
* Maximum order count.
* Customers using more than five coupons.
* Order categories associated with higher coupon usage.

### 💳 Payment Behaviour

* Most preferred payment method among active customers.
* Average number of registered devices among customers using UPI.
* Payment methods associated with specific customer conditions.

### ⭐ Customer Satisfaction

* Maximum satisfaction score.
* Total orders placed by customers using credit cards with the highest satisfaction score.
* Average satisfaction score among customers who submitted complaints.

### 💰 Cashback Analysis

The project calculates the average cashback by preferred order category and identifies the top categories based on average cashback.

### 📍 Distance Analysis

Customers are categorized according to their warehouse-to-home distance:

```text
Very Close Distance
Close Distance
Moderate Distance
Far Distance
```

The analysis then compares these distance categories with customer churn status.

---

## 🔁 Customer Returns Analysis

A separate `customer_returns` table is created containing:

* Return ID
* Customer ID
* Return date
* Refund amount

The project then joins the returns data with the customer churn data to identify returned orders associated with customers who:

* Have churned
* Have submitted complaints

This demonstrates the use of SQL JOIN operations for combining related datasets.

---

## 🧠 SQL Concepts Used

This project demonstrates practical use of:

* `CREATE DATABASE`
* `CREATE TABLE`
* `INSERT INTO`
* `ALTER TABLE`
* `UPDATE`
* `DROP COLUMN`
* `SELECT`
* `WHERE`
* `GROUP BY`
* `ORDER BY`
* `LIMIT`
* `DISTINCT`
* `CASE`
* Aggregate functions

  * `COUNT()`
  * `SUM()`
  * `AVG()`
  * `MAX()`
* `ROUND()`
* Subqueries
* Conditional aggregation
* Percentage calculations
* `INNER JOIN`
* Data transformation
* Exploratory data analysis

---

## 🛠️ Tools Used

| Tool                | Purpose                             |
| ------------------- | ----------------------------------- |
| **MySQL**           | Database creation and SQL analysis  |
| **MySQL Workbench** | Writing and executing SQL queries   |
| **GitHub**          | Project documentation and portfolio |

---

## 📂 Project Structure

```text
E-Commerce-Customer-Churn-Analysis/
│
├── E-Commerce_Customer_Churn_Analysis.sql
└── README.md
```

---

## ▶️ How to Run the Project

### 1. Install MySQL

Use **MySQL Workbench** or another MySQL-compatible environment.

### 2. Open the SQL file

Open:

```text
E-Commerce_Customer_Churn_Analysis.sql
```

### 3. Execute the script

Run the SQL script from top to bottom.

The script will:

1. Create the `ecomm` database.
2. Create the `customer_churn` table.
3. Insert the customer data.
4. Perform data preparation and transformations.
5. Execute customer churn analysis queries.
6. Create the `customer_returns` table.
7. Perform the customer returns analysis.

### 4. Explore the results

Execute individual queries to view the results of each analysis.

---

## 📊 Key Business Areas Explored

```text
Customer Churn
      ↓
Customer Behaviour
      ↓
Orders & Purchasing Patterns
      ↓
Payment Preferences
      ↓
Customer Complaints
      ↓
Satisfaction
      ↓
Coupons & Cashback
      ↓
Returns & Refunds
```

---

## 💡 Skills Demonstrated

Through this project, I demonstrated practical skills in:

* SQL querying
* Data cleaning and transformation
* Exploratory data analysis
* Customer churn analysis
* Aggregation and filtering
* Business-oriented problem solving
* Relational data analysis
* SQL joins and subqueries
* Converting raw data into meaningful business information

---

## 👩‍💻 Author

**Gayathri S Pillai**

Aspiring Data Analyst | MBA – Business Analytics & Marketing


