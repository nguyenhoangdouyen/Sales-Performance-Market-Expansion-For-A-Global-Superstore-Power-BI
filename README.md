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

![Image](https://github.com/user-attachments/assets/1de1af20-fa92-4de9-8c2c-7219f043272d)

### 📌 Key Findings:

The overview dashboard reveals several key highlights regarding Global Superstore’s overall business performance:

#### 🚀 1. Strong growth in both Revenue & Profit
- **Total revenue** reached **$9.48M**, a significant **+51.3% increase** compared to last year.
- **Profit** also rose proportionally to **$1.09M**, while the **profit margin remained stable at 12%**.
- Despite strong top-line growth, the profit margin did not improve — indicating rising costs or unchanged operational efficiency.

#### 👥 2. Heavy reliance on returning customers
- While **orders increased by 51.7%**, the number of **unique buyers only grew by 1%**.
- **99.97% of revenue came from existing customers**, showing an extremely loyal customer base but limited new acquisition.

#### 🌍 3. Market & category performance varies
- **APAC, EU, and US** contributed the most to overall revenue.
- However, **Canada** stood out with the **highest profit margin (28%)**, despite lower revenue.
- On the other hand, **EMEA and Africa** underperformed with low revenue and slim profit margins.

#### 📦 4. Technology leads product category growth
- The **Technology category** showed the most noticeable revenue growth over the previous year.
- **Office Supplies** and **Furniture** experienced minor increases but at a slower pace.

#### 🏠 5. Consumer segment dominates
- The **Consumer segment accounted for over half of total revenue ($4.9M)**, far ahead of Corporate ($2.9M) and Home Office ($1.7M).
- Profit margins across segments were fairly consistent (~11–12%), with no standout differences in profitability.

### II. Market Analysis



### 📌 Key Findings:



### III. Product Analysis



### 📌 Key Findings:



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




