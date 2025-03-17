# 📊 Project Title: Global Superstore Sales Performance & Market Expansion | Retail Analytics | Power BI

**Author:** Nguyễn Hoàng Đỗ Uyên

**Date:** March 2025

**Tools Used:** BI

## 📌 Background & Overview

**Objective:**

**📖 What is this project about?**

The objective is to:
- Optimize market expansion strategies.
- Identify strategic products for growth.
- Provide data-driven insights to improve decision-making.


**👤 Who is this project for?**

✔️ Data analysts & business analysts seeking actionable insights.

✔️ Marketing and sales teams focusing on product performance and market growth.

✔️ Route to market team aiming to improve distribution strategies and market reach.


**❓Business Questions:**

✔️ What is the current performance of Superstore?

✔️ Which markets should Superstore expand into to increase revenue and ROI?

✔️ Which products should be prioritized for strategic growth?


**🎯Project Outcome:**

## 📂 Dataset Description & Data Structure

### **📌 Data Source** 

- **Source**: Kaggle  
- **Size**: The **Orders** table contains **51,290** records.  
- **Format**: CSV  

### 📊 **Data Structure & Relationships**  

#### 1️⃣ **Tables Used:**  
The dataset consists of **three tables**:  

- 🛒 **Orders** – Contains detailed transaction and customer information (**51,290 records**).  
- 🔄 **Returns** – Stores data on returned orders.  
- 👥 **People** – Holds information about sales representatives.  

#### **2️⃣ Table Schema & Data Snapshot**

**Table 1**: Orders 

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

**Table 2**: People

| Column Name | Data Type | Description |
|-------------|----------|-------------|
| `Person`    | `VARCHAR` | Name of the salesperson. |
| `Region`    | `VARCHAR` | Geographic region where the salesperson operates. |

**Table 3**: Returns

| Column Name  | Data Type | Description |
|-------------|----------|-------------|
| `Returned`  | `VARCHAR` | Indicates whether the order was returned (e.g., 'Yes' or 'No'). |
| `Order ID`  | `VARCHAR` | Unique identifier for each order. |

#### 3️⃣ Data Relationships:

![Image](https://github.com/user-attachments/assets/ea814a90-0f20-4b7d-9cb1-929e79163978)

### 🧠 Design Thinking Process

#### 1️⃣ Empathize

![Image](https://github.com/user-attachments/assets/31ed7661-a5b5-4aa4-a668-b82f7a158f20)

![Image](https://github.com/user-attachments/assets/d1daa54c-ed85-4390-86a2-ef683459f902)

#### 2️⃣ Define point of view 

![Image](https://github.com/user-attachments/assets/3c38e19a-d362-4770-8571-35b1e3d5133f)

#### 3️⃣ Ideate

![Image](https://github.com/user-attachments/assets/b7451df3-d4de-4b81-9f02-94eff089f10c)

#### 4️⃣ Prototype and review

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

### 🟡 Conclusion: 

#### **Revenue & Profit Performance**  
- **Total revenue** reached **$9.48M**, with **$1.09M profit** and **25K orders**. Despite **steady revenue growth**, **profit stagnated in 2014**, suggesting **rising costs or declining margins**.  
- **ROI declined to 11.50%** in 2014, indicating that **profitability did not scale proportionally** with revenue.  

#### **Market & Customer Trends**  
- **APAC** generated the **highest profit ($531.77K)** but also had the **highest return rate (5.45%)**, whereas **EU** maintained **lower profit ($332.26K)** but with a **more stable return rate (0.85%)**.  
- **Canada had the highest ROI (13%)**, while the **US lagged behind at just 1%**, highlighting **profitability challenges** in the US market.  
- **Returning customers** contributed the majority of revenue, reflecting **strong brand loyalty**, but **new customer acquisition remained low**, limiting **market expansion opportunities**.  

#### **Category & Product Performance**  
- **Technology** led in revenue, growing from **$520K (2011) to $1.25M (2014)**, but **profitability fluctuated** due to **higher return rates**.  
- **Office Supplies** remained a **stable category** with **steady profit growth**, driven by **low-return products** like **Binders, Paper, and Labels**.  
- **Furniture** showed **volatile revenue**, with **Tables & Bookcases** facing **high return rates**, impacting long-term profitability.  
- **Top revenue-generating products** included **Cisco Smartphones, Motorola Smartphones, and Canon Copiers**, with **Canon Copiers delivering the highest per-unit profit**.  

#### **Operational Risks & Growth Challenges**  
- **Return rates improved**, declining from **6.36% (2011) to 5.41% (2014)**, but **APAC's high return rate remains a risk**.  
- **Profit stagnation in 2014** suggests **operational inefficiencies or increased cost structures**, requiring **cost control measures** to sustain long-term profitability.  


