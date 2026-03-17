# E-commerce-Customer-Churn-Analysis-
**PROJECT OVERVIEW**

This project focuses on analyzing customer churn patterns in the e-commerce sector using SQL. The main objective is to identify the key factors that lead to customer churn—such as tenure, complaints, payment methods, and ordering behavior—and to generate meaningful insights that can help businesses reduce customer attrition.

**TOOLS USED**

* **MySQL** – Used for data cleaning, transformation, and analysis
* **SQL Workbench** – Used for executing and testing SQL queries

**DATASET**

Source: https://drive.google.com/uc?export=download&id=1iKKCze_Fpk2n_g3BIZBiSjcDFdFcEn3D

**Important Columns:**
CustomerID, Tenure, PreferredPaymentMode, PreferredOrderCat, CityTier, WarehouseToHome, HoursSpentOnApp, OrderCount, CouponUsed, SatisfactionScore, CashbackAmount, Churn, Complain

**STEPS PERFORMED**

**1. Data Cleaning**

* Handled missing values by filling numeric columns with the **mean** and categorical columns with the **mode**.
* Removed extreme outliers in the **WarehouseToHome** column where the distance exceeded 100 km.
* Standardized inconsistent categorical values (for example, converting **“COD”** to **“Cash on Delivery”**).

**2. Data Transformation**

* Corrected inconsistent column names (for example, **PreferedOrderCat → PreferredOrderCat**).
* Generated new derived fields:

  * **ComplaintReceived** (Yes/No)
  * **ChurnStatus** (Active/Churned)
* Removed unnecessary columns such as **Churn** and **Complain** after transformation.

**3. Data Exploration & Analysis**

* Calculated the number of churned versus active customers.
* Analyzed the **average tenure and cashback amount** of churned customers.
* Examined churn patterns based on **complaints, city tier, and preferred order category**.
* Identified the **most common payment method among active customers**.
* Performed customer segmentation using **marital status, warehouse distance, and satisfaction score**.
* Found the **top three order categories with the highest average cashback**.
* Grouped customers by warehouse distance categories: **Very Close, Close, Moderate, and Far**.

**4. Relational Table Design**

* Created an additional table named **customer_returns** to monitor product return and refund behavior.
* Joined this table with the customer dataset to analyze churn patterns among customers who had both **complaints and returns**.

**KEY INSIGHTS**

* Customers who registered complaints had a **much higher likelihood of churning**.
* **City Tier-1** recorded the highest churn rate in the **Laptop & Accessories** category.
* **Credit Card** emerged as the most preferred payment method among active customers.
* **Single customers** who preferred **mobile phone purchases** showed higher order value growth.
* The top cashback-generating categories were **Electronics, Fashion, and Groceries**.
* **Warehouse distance had a strong impact on churn**, with customers located farther from warehouses showing higher churn rates.
