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
<summary> <strong>Table 1: Orders</strong></summary>

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
<summary> <strong>Table 2: Returns</strong></summary>

| Column Name  | Data Type | Description |
|--------------|-----------|-------------|
| `Returned`   | `VARCHAR` | Indicates whether the order was returned (e.g., 'Yes' or 'No'). |
| `Order ID`   | `VARCHAR` | Unique identifier for each order. |

</details>
  
- 👥 **People** – Holds information about sales representatives.

<details>
<summary> <strong>Table 3: People</strong></summary>

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

![Image](https://github.com/user-attachments/assets/ff5ae83c-f1c5-4dba-b975-cf68294b0518)

![Image](https://github.com/user-attachments/assets/fe8ffc6a-f69c-4d6e-b66e-0b7721097c6c)

![Image](https://github.com/user-attachments/assets/247419e0-710f-4791-b49b-6a434444df72)

![Image](https://github.com/user-attachments/assets/f279dd3a-a5d5-4823-950b-443523ad619f)

### 2️⃣ Define point of view 

![Image](https://github.com/user-attachments/assets/7a4e2fe0-8db3-4c70-84de-27bdce73bb8d)

![Image](https://github.com/user-attachments/assets/874b6351-0d0b-40a0-a9ae-6ca4d985dff4)

### 3️⃣ Ideate

![Image](https://github.com/user-attachments/assets/d2593003-8ca6-4556-a011-7ee4f576a46d)

![Image](https://github.com/user-attachments/assets/217eb049-5a4d-4acb-bb50-7cd34c58ff25)

### 4️⃣ Prototype and review

This part is in the dashboard

## 📊 Key Insights & Visualizations

### 🔍 Dashboard Preview

### I. Overview

![Image](https://github.com/user-attachments/assets/ef336a3e-0280-4598-a55f-50fe3e2ac02b)

### 📌 Key Findings:

The overview dashboard reveals several key highlights regarding Global Superstore’s overall business performance:

#### 🚀 Strong growth in both Revenue & Profit
- **Total revenue** reached **$9.48M**, a significant **+51.3% increase** compared to last year.
- **Profit** also rose proportionally to **$1.09M**, while the **profit margin remained stable at 12%**.
- Despite strong top-line growth, the profit margin did not improve — indicating rising costs or unchanged operational efficiency.

#### 👥 Heavy reliance on returning customers
- While **orders increased by 51.7%**, the number of **unique buyers only grew by 1%**.
- **99.97% of revenue came from existing customers**, showing an extremely loyal customer base but limited new acquisition.

#### 🌍 Market & category performance varies
- **APAC, EU, and US** contributed the most to overall revenue.
- However, **Canada** stood out with the **highest profit margin (28%)**, despite lower revenue.
- On the other hand, **EMEA and Africa** underperformed with low revenue and slim profit margins.

#### 📦 Technology leads product category growth
- The **Technology category** showed the most noticeable revenue growth over the previous year.
- **Office Supplies** and **Furniture** experienced minor increases but at a slower pace.

#### 🏠 Consumer segment dominates
- The **Consumer segment accounted for over half of total revenue ($4.9M)**, far ahead of Corporate ($2.9M) and Home Office ($1.7M).
- Profit margins across segments were fairly consistent (~11–12%), with no standout differences in profitability.

### II. Market Analysis

![Image](https://github.com/user-attachments/assets/23e1875d-8cbf-413b-9c0f-03a707ef6c88)

### 📌 Key Findings:

#### 💰 Revenue and Profit Distribution  
- **Total revenue** reached **$9.48M**, with **APAC** contributing the most (**$2.7M**), followed by **EU ($2.1M)** and **US ($1.8M)**.  
- **Canada**, despite generating only **$0.1M**, recorded the **highest profit margin (28%)**, indicating strong operational efficiency on a small scale.  
- In contrast, **EMEA** and **Africa** underperformed with low revenue and slim profit margins (~6–12%), dragging down overall performance.

#### 📊 Profit Contribution by Market (2011–2014)  
- Over the 4-year period, **APAC, EU, and US** consistently contributed the most to total profit.  
- **LATAM** maintained a steady contribution (~15%), while **Africa** and **Canada** made minor, stagnant contributions.

#### 📈 Revenue Growth by Market & Category (YoY%)  
- **Canada** led in revenue growth with a **+219.5% YoY increase**, especially in the **Technology category (+63.5%)**.  
- Emerging markets like **EMEA (+183.15%)** and **Africa (+168.25%)** also saw rapid growth, indicating expansion potential.  
- Meanwhile, mature markets such as **US, EU, and APAC** showed steady growth (144–157%) but at a slower pace than developing regions.

#### 👥 Customer Base by Region  
- **Central, South, and EMEA** had the highest number of **returning customers**, reflecting strong customer loyalty.  
- **Oceania** stood out with the **largest number of new customers (187)**, indicating growth potential in customer acquisition.

#### 📦 Order Quantity & Return Rate  
- **Central** led in both **order volume** and **lowest return rate (~1%)**, highlighting operational efficiency.  
- Other regions maintained a stable return rate (1–3%) without any alarming figures.

#### 🧑‍💼 Employee Productivity by Region  
- **Central** stood out in employee productivity with:  
  → **Revenue per employee**: $2.07M  
  → **Profit per employee**: $212K  
  → **Orders per employee**: 5,237  
- **Canada**, on the other hand, recorded the lowest across all three indicators, consistent with its low revenue and profit contribution.

### III. Product Analysis

![Image](https://github.com/user-attachments/assets/aa9b8966-1db7-4a2b-afbf-5d2e8034b6ee)

### 📌 Key Findings:

#### 📌 Quadrant Analysis by Sub-Category  
- This chart gives the most comprehensive overview by classifying product performance across two axes: **Revenue** and **Profit Margin**.  
- **Copiers** and **Phones** are top performers, sitting in the top-right quadrant with **high revenue** and **strong profit margins** – clear leaders.  
- **Accessories**, **Art**, and **Labels** have **high profit margins** but **low revenue** – they’re **profitable but under-scaled**, showing potential for growth.  
- **Chairs**, **Bookcases**, and **Storage** show **decent revenue** but **low margins**, meaning they sell well but don’t earn much.  
- Bottom-left quadrant features the underperformers: **Supplier** and **Furnishings** – **low revenue + low margins**, likely dragging down overall performance.

#### 💰 Revenue and Profit Margin by Sub-Category  
- In terms of revenue, **Phones ($1.4M)**, **Chairs**, **Copiers**, and **Tables** are leading.  
- Looking at profit margin, standouts include: **Accessories (26%)**, **Labels (23%)**, and **Art (18%)** – small but highly profitable.  
- Meanwhile, **Tables (-7%)** is underperforming with minimal or negative profits.

#### 📦 Orders, Customers, and Return Rate by Sub-Category  
- **Storage** has the highest number of orders (**216**), followed by **Phones (91)** and **Chairs (86)** – aligning with high-revenue categories.  
- But high order count ≠ high profitability: **Storage**, for example, has low profit margins despite strong sales.  
- **Labels (10%)**, **Fasteners (6%)**, and **Paper (5%)** have high return rates – red flags for quality or customer expectation issues.  
- In contrast, categories like **Art**, **Appliances**, and **Binders** have **near-zero return rates**, indicating a solid customer experience.

#### 🚚 Revenue and Profit by Ship Mode  
- **Standard Class** dominates with **$5.7M in revenue**, far surpassing other shipping modes.  
- **First Class** and **Second Class** bring in significantly less revenue (**$1.4M**, **$1.9M**) and lower profits – suggesting most customers prioritize cost over speed.

#### 🪑 Profit by Segment and Category  
- **Consumer Segment** generates the highest profit (**$0.28M**), outperforming Corporate and Home Office.  
- Within each segment, **Technology** consistently delivers the most profit, especially for Consumer and Corporate.  
- **Office Supplies**, however, yield lower profit margins – especially in the Home Office segment, which is barely profitable.

#### 🏆 Top 10 Products by Profit  
- Products from **Canon imageCLASS 2200 Advance Copier, Motorola Smart Phone Fullsize, Cisco Smart Full Size**, etc., top the profit chart – mostly from the **Technology** category, indicating high value with fewer units.  
- A few Furniture and Office Supplies products made the list, but they lag behind their tech counterparts in profitability.

## 🔎 Final Conclusion & Recommendation 

## ✨ Conclusion: 



## ✨ Recommendation: 



