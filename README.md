# 🌍 Sales Performance & Market Expansion For A Global Superstore | Power BI

![image](https://github.com/user-attachments/assets/65df4f32-c787-4986-856f-49ef3f9034b6)

**Author:** Nguyễn Hoàng Đỗ Uyên

**Date:** March 2025

**Tools Used:** BI

## Table of Contents
1. [📌 Background & Overview](#background--overview)
2. [📂 Dataset Description & Data Structure](#dataset-description--data-structure)
3. [🧠 Design Thinking Process](#design-thinking-process)
4. [📊 Key Insights & Visualizations](#key-insights--visualizations)
5. [🔎 Final Conclusion & Recommendation](#final-conclusion--recommendation)

---

## 📌 Background & Overview

**Objective:**

**📖 What is this project about?**

This project aims to build a **Power BI dashboard** using the *Global Superstore Sales* dataset, which includes data on transactions (**Orders**), sales representatives (**People**), and product returns (**Returns**).
The goal is to provide senior managers with **data-driven insights** to:

- **Understand current business performance**
 
- **Optimize market expansion strategies**

- **Identify strategic products for growth**

- **Support better decision-making to drive revenue and ROI**


**👤 Who is this project for?**

✔️ Data analysts & business analysts seeking actionable insights.

✔️ Marketing and sales teams focusing on product performance and market growth.

✔️ Route to market team aiming to improve distribution strategies and market reach.


**❓Business Questions:**

✔️ What is the current performance of Superstore?

✔️ Which markets should Superstore expand into to increase revenue and ROI?

✔️ Which products should be prioritized for strategic growth?


**🎯Project Outcome:**

- Revenue grows but profit stagnates, signaling rising costs & declining margins, especially in 2014.  
- APAC & EU drive profitability, but APAC faces high return risks, while the US struggles with low ROI.  
- Technology leads revenue, but high return rates impact margins. Office Supplies provide stable growth, and Furniture faces profitability challenges due to logistics issues.  
- Canon Copiers are the most profitable per unit, while Cisco & Motorola Smartphones need return management strategies.  
- Market expansion should focus on EU & profitable APAC regions, while US operations need profitability optimization.  

By aligning market and product strategies, senior management can **prioritize high-potential regions**, **optimize pricing & cost structures**, and **reduce return risks**, ensuring **sustainable revenue & profit growth**.  

## 📂 Dataset Description & Data Structure

### **📌 Data Source** 

- **Source**: Kaggle  
- **Size**: The **Orders** table contains **51,290** records.  
- **Format**: CSV  

### 📊 **Data Structure & Relationships**  

#### 1️⃣ **Tables Used:**  
The dataset consists of **three tables**:  

- 🛒 **Orders** – Contains detailed transaction and customer information (**51,290 records**).

<details>
<summary>📦 <strong>Table 1: Orders</strong></summary>

| Column Name       | Data Type   | Description                              |
|------------------|------------|------------------------------------------|
| `Order ID`      | `VARCHAR`   | Unique identifier for each order.       |
| `Order Date`    | `DATE`      | Date when the order was placed.         |
| `Ship Date`     | `DATE`      | Date when the order was shipped.        |
| `Ship Mode`     | `VARCHAR`   | Shipping method used for delivery.      |
| `Customer ID`   | `VARCHAR`   | Unique identifier for each customer.    |
| `Customer Name` | `VARCHAR`   | Full name of the customer.              |
| `Segment`       | `VARCHAR`   | Customer segment (e.g., Consumer, Corporate). |
| `City`         | `VARCHAR`   | City where the order was placed.        |
| `State`        | `VARCHAR`   | State where the order was placed.       |
| `Country`      | `VARCHAR`   | Country where the order was placed.     |
| `Postal Code`  | `VARCHAR`   | Postal code of the shipping address.    |
| `Market`       | `VARCHAR`   | Market region (e.g., APAC, EMEA).       |
| `Region`       | `VARCHAR`   | Geographical region of the order.       |
| `Product ID`   | `VARCHAR`   | Unique identifier for each product.     |
| `Category`     | `VARCHAR`   | Product category (e.g., Furniture, Office Supplies). |
| `Sub-Category` | `VARCHAR`   | Sub-category of the product.            |
| `Product Name` | `VARCHAR`   | Name of the product ordered.            |
| `Sales`        | `DECIMAL`   | Revenue generated from the order.       |
| `Quantity`     | `INT`       | Number of items ordered.                |
| `Profit`       | `DECIMAL`   | Profit earned from the order.           |

</details>

- 🔄 **Returns** – Stores data on returned orders.

<details>
<summary>↩️ <strong>Table 3: Returns</strong></summary>

| Column Name  | Data Type | Description |
|--------------|-----------|-------------|
| `Returned`   | `VARCHAR` | Indicates whether the order was returned (e.g., 'Yes' or 'No'). |
| `Order ID`   | `VARCHAR` | Unique identifier for each order. |

</details>
  
- 👥 **People** – Holds information about sales representatives.

<details>
<summary>🧑‍💼 <strong>Table 2: People</strong></summary>

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| `Person`    | `VARCHAR` | Name of the salesperson. |
| `Region`    | `VARCHAR` | Geographic region where the salesperson operates. |

</details>

#### 2️⃣ Data Relationships:

![Image](https://github.com/user-attachments/assets/ea814a90-0f20-4b7d-9cb1-929e79163978)

| **From Table** | **To Table** | **Join Key**   | **Relationship Type**                                  |
|------------|----------|------------|----------------------------------------------------|
| `Orders`   | `People` | `Region`   | Many-to-One (multiple orders belong to one region) |
| `Orders`   | `Returns`| `Order ID` | One-to-One or Left Join (not all orders are returned) |

## 🧠 Design Thinking Process

### 1️⃣ Empathize

![Image](https://github.com/user-attachments/assets/31ed7661-a5b5-4aa4-a668-b82f7a158f20)

![Image](https://github.com/user-attachments/assets/d1daa54c-ed85-4390-86a2-ef683459f902)

### 2️⃣ Define point of view 

![Image](https://github.com/user-attachments/assets/3c38e19a-d362-4770-8571-35b1e3d5133f)

### 3️⃣ Ideate

![Image](https://github.com/user-attachments/assets/b7451df3-d4de-4b81-9f02-94eff089f10c)

### 4️⃣ Prototype and review

This part is in the dashboard

## 📊 Key Insights & Visualizations

### 🔍 Dashboard Preview

### I. Overview

![Image](https://github.com/user-attachments/assets/7688db58-8ca6-4cde-aad0-8a6c324ff7ea)

### 📌 Key Findings:

**Overall Business Performance**  
- Total revenue: **$9.48M**, profit: **$1.09M**, with **25K orders**.  
- AOV: **$378.52**, ROI: **11.50%**.  
- Revenue grows steadily, but profit stagnates in **2014**, indicating rising costs or declining margins.  

**Customer Analysis**  
- Returning customers outnumber new customers, reflecting a loyal customer base.  
- New customer acquisition remains low, suggesting limited market expansion.  
- Returning customers contribute most of the revenue, indicating repeat purchase behavior and stable cash flow.  
- New customers generate lower revenue, possibly due to lower purchase frequency or smaller order values.  

**Revenue & Profit Trends by Year**
- Revenue increased from **$1.68M (2011) to $3.21M (2014)**, nearly doubling, but growth slowed down.  
- Profit growth was inconsistent, with **2014 showing stagnation**, likely due to increased costs or declining profit margins.  
- ROI declined in **2014**, indicating profit did not scale proportionally with revenue.  

### II. Market Analysis

![Image](https://github.com/user-attachments/assets/9659dfdb-e206-4234-82ef-ec67a584f1cf)

### 📌 Key Findings:

- Total Revenue: **$9.48M**, Profit: **$1.09M**, ROI: **12%**. Revenue grows, but profit stagnates in 2014, indicating rising costs or declining margins.  
- APAC leads in profit (**$531.77K**) but has the highest return rate (**5.45%**), while EU profits less (**$332.26K**) but maintains a lower return rate (**0.85%**).  
- Return rates decline from **6.36% (2011) to 5.41% (2014)**.  
- ROI by market: Canada tops at **13%**, while the US lags at **1%**, showing a profitability gap.  
- Top revenue regions: South, Central, Oceania, North, and Southeast Asia.  
- Profit growth fluctuates, with 2014 showing stagnation despite revenue growth.  
- APAC and EU drive revenue and profit, but APAC sees higher return risks, while the US struggles with low ROI.  

### III. Product Analysis

![Image](https://github.com/user-attachments/assets/caf3fa51-42f1-4acf-9a89-dcfbfa334b8c)

### 📌 Key Findings:
- **Top 10 products** by revenue & profit: **Cisco Smartphones, Motorola Smartphones, Canon Copiers** lead.  
- **Technology** has the **highest revenue** but also a **higher return rate**, impacting profitability.  
- **Office Supplies** maintains **steady revenue** and **low return rates**, making it a stable category.  
- **Furniture** has **moderate revenue** but **higher return risks**, likely due to logistics or product defects.  
- **Technology** revenue increased from **$520K (2011) to $1.25M (2014)**, peaking in **2014**, but profit margins fluctuated due to higher return rates.  
- **Office Supplies** shows consistent profit growth, driven by **Binders, Paper, Labels**, which have low return rates.  
- **Furniture** revenue is volatile, with **Tables & Bookcases** having higher return rates, impacting profitability in later years.  
- **Canon Copiers, Cisco Smartphones, Motorola Smartphones** are among the top revenue-generating products, with **Canon Copiers** delivering the highest per-unit profit.  


## 🔎 Final Conclusion & Recommendation 

## ✨ Conclusion: 

#### 🟡 **Revenue & Profit Performance**  
- **Revenue** has **grown steadily**, but **profit** did not scale accordingly, suggesting **rising costs** or **declining margins**.  
- Some **markets** generate strong **revenue** but struggle with **low profitability**, highlighting inefficiencies in **cost management** or **pricing strategies**.  

#### 🌍📊 **Market & Customer Trends**  
- **APAC** and the **EU** are **key revenue drivers**, but **APAC** faces **higher return risks**, while the **US** struggles with **low ROI**.  
- The business relies heavily on **returning customers**, indicating **strong loyalty** but also **limited market expansion**.  

#### 🏷️📦 **Product & Category Trends**  
- **Technology** is the **dominant revenue driver** but faces **profitability challenges** due to **high return rates**.  
- **Office Supplies** provide **stable revenue** with **low returns**, making it a **reliable category**.  
- **Furniture** is **riskier**, with **fluctuating revenue** and **high return rates**, likely due to **logistical challenges** or **product defects**.  
- **High-margin products**, like **Canon Copiers**, contribute significantly to **profitability**, while **smartphones** generate **strong revenue** but face **higher return risks**.  

## ✨ Recommendation: 

#### 🌍 **Market Expansion Strategy**  
- **Canada & EU**: Focus on **expansion & retention** since these markets have **high ROI & low return rates**. Strengthen **regional partnerships** and increase investment in **Office Supplies**, which show **steady demand & profitability**.  
- **US**: Address **low ROI** by **optimizing costs** (e.g., logistics & discount strategies) and refining **pricing models**. Strengthen **customer retention programs** to maximize lifetime value.  
- **APAC**: Despite **high revenue**, the market struggles with **high return rates**. Improve **product quality control** and streamline **after-sales service** to enhance profitability. Consider **localized marketing strategies** for better engagement.  
- **LATAM & Canada**: These regions contribute **lower revenue**, so explore **targeted promotions** or **bundled product offers** to increase order volume.  

#### 🏆 **Strategic Product Selection**  
- **Canon Copiers**: Prioritize due to **high per-unit profit** and **consistent demand**. Expand marketing efforts in **underperforming regions** to increase sales.  
- **Cisco Smartphones**: A **top revenue driver** but faces **return challenges**. Implement **extended warranties** and **repair programs** to improve customer trust and reduce returns.  
- **Office Supplies (Binders & Paper)**: A **stable revenue stream** with **low return rates**. Leverage as a **cross-selling opportunity** with **high-margin tech products** to boost profitability.  

#### 🔄 **Customer Growth & Retention**  
- **New Customer Acquisition**: Invest in **targeted marketing campaigns** in **LATAM & Canada** to drive sales growth. Offer **introductory discounts** or **loyalty incentives**.  
- **Returning Customers**: Strengthen **loyalty programs** with **exclusive discounts** on repeat purchases. Promote **higher-order value bundles** to maximize customer lifetime value.  
- **Cross-sell & Upsell**: Use data-driven recommendations to suggest complementary products (e.g., **Office Chairs with Desks**, **Paper with Printers**).  




