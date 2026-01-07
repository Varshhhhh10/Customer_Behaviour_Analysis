# 🛍️ Customer Shopping Behavior Analysis

**End-to-End Data Analytics Project (Python | SQL | PostgreSQL | Power BI)**

---

## 📌 Project Overview

This project analyzes **customer shopping behavior** for a retail company to uncover insights that help improve:

* Sales performance
* Customer engagement
* Long-term loyalty
* Marketing and product strategy

The analysis is performed using **Python for data preparation**, **SQL (PostgreSQL) for business queries**, and **Power BI for visualization**.

---

## 🎯 Business Problem Statement

A leading retail company observed changes in:

* Purchasing patterns
* Customer demographics
* Product preferences
* Online vs offline shopping behavior

### Key Business Question:

> **How can consumer shopping data be leveraged to identify trends, improve customer engagement, and optimize marketing and product strategies?**

---

## 🧾 Dataset Summary

* **Total Records:** 3,900 purchases
* **Total Columns:** 18
* **Data Type:** Transactional customer shopping data

### Key Features:

* Customer demographics: Age, Gender, Location
* Purchase details: Item, Category, Amount, Season
* Behavior metrics: Discounts, Previous Purchases, Frequency
* Customer feedback: Review Ratings
* Subscription & shipping information

---

## 🧹 Data Preparation & Cleaning (Python)

### Tools Used

* Python
* Pandas
* NumPy
* PostgreSQL (database integration)

### Key Steps:

1. Loaded raw dataset using Pandas
2. Performed initial inspection using:

   * `df.info()`
   * `df.describe()`
3. **Handled missing values**

   * 37 missing values in `review_rating`
   * Imputed using **median rating per product category**
4. **Column standardization**

   * Converted column names to `snake_case`
5. **Feature Engineering**

   * Created `age_group` by binning ages
   * Derived `purchase_frequency_days`
6. **Data consistency check**

   * Removed redundant column `promo_code_used`
7. Loaded cleaned data into **PostgreSQL**

👉 *This step ensures SQL-ready, analysis-friendly data.*

---

## 🗄️ Database & SQL Analysis (PostgreSQL)

The cleaned dataset was stored in PostgreSQL to simulate **real business transactions**.

### Key SQL Concepts Used:

* CTEs (`WITH` clause)
* Aggregations (`SUM`, `COUNT`, `AVG`)
* CASE statements
* Window functions (ranking)
* GROUP BY & HAVING

---

## 📊 Key Business Analyses Performed (SQL)

### 1️⃣ Revenue by Gender

* Compared total revenue between male and female customers

### 2️⃣ High-Spending Discount Users

* Identified customers who:

  * Used discounts
  * Still spent **above average purchase amount**

### 3️⃣ Top 5 Products by Average Rating

* Ranked products using average `review_rating`

### 4️⃣ Shipping Type Comparison

* Compared average purchase amounts for:

  * Standard shipping
  * Express shipping

### 5️⃣ Subscribers vs Non-Subscribers

* Compared:

  * Total customers
  * Average spend
  * Total revenue

### 6️⃣ Discount-Dependent Products

* Identified products with **highest percentage of discounted purchases**

### 7️⃣ Customer Segmentation (Important for Interviews ⭐)

Customers were classified as:

* **New:** 1 previous purchase
* **Returning:** 2–10 purchases
* **Loyal:** More than 10 purchases

👉 Implemented using SQL `CASE` + `CTE`.

### 8️⃣ Top 3 Products per Category

* Ranked products within each category based on order count

### 9️⃣ Repeat Buyers & Subscriptions

* Checked whether customers with **>5 purchases** are more likely to subscribe

### 🔟 Revenue by Age Group

* Compared revenue contribution across age groups

---

## 📈 Visualization (Power BI)

An interactive **Customer Behavior Dashboard** was built using Power BI.

### Dashboard Highlights:

* Total customers (3.9K)
* Average purchase amount
* Average review rating
* Revenue by category
* Sales by age group
* Subscription distribution
* Shipping preference insights

👉 This helps **non-technical stakeholders** quickly understand trends.

---

## 💡 Business Insights & Recommendations

### 🔹 Boost Subscriptions

* Promote exclusive subscriber benefits
* Loyal customers show long-term value

### 🔹 Customer Loyalty Programs

* Incentivize repeat buyers to move into **Loyal** segment

### 🔹 Review Discount Strategy

* Balance discounts with profitability

### 🔹 Product Positioning

* Highlight:

  * Top-rated products
  * Best-selling items

### 🔹 Targeted Marketing

* Focus campaigns on:

  * High-revenue age groups
  * Express-shipping users

---

## 🛠️ Tech Stack

| Layer           | Tools                  |
| --------------- | ---------------------- |
| Data Cleaning   | Python (Pandas, NumPy) |
| Database        | PostgreSQL             |
| Querying        | SQL                    |
| Visualization   | Power BI               |
| Version Control | Git & GitHub           |

---


## 🎤 Interview Revision Tips

When explaining this project:

* Start with **business problem**
* Explain **why each tool was used**
* Highlight **customer segmentation logic**
* Mention **real-world decision making**
* Emphasize **end-to-end ownership**


