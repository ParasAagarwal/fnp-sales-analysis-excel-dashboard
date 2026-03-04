# FNP Sales Analysis (Excel Dashboard)

## Project Overview

This project analyzes sales data from **Ferns & Petals (FNP)**, a gifting platform specializing in delivering gifts for occasions such as **Diwali, Raksha Bandhan, Holi, Valentine's Day, Birthdays, and Anniversaries**.

The goal of this analysis is to uncover insights related to **sales performance, customer behavior, product popularity, and delivery efficiency** using **Microsoft Excel, Power Query, and Power Pivot**.

The final output of this project is an **interactive Excel dashboard** designed to help business stakeholders understand key metrics and trends.

---

## Business Problem

FNP wants to better understand its business performance in order to:

- Identify high-performing products
- Analyze seasonal sales trends
- Understand customer spending behavior
- Evaluate delivery performance
- Identify cities with the highest order volume
- Compare revenue across different occasions

---

## Dataset Description

The dataset contains information related to **orders, products, and customers**.

### Orders
- Order ID  
- Customer ID  
- Product ID  
- Order Date  
- Delivery Date  
- Order Time  
- Delivery Time  
- Quantity  
- Occasion  

### Products
- Product ID  
- Product Name  
- Category  
- Price (INR)

### Customers
- Customer ID  
- Customer Name  
- City

---

## Tools Used

| Tool | Purpose |
|-----|--------|
| Microsoft Excel | Data analysis |
| Power Query | Data extraction and cleaning |
| Power Pivot | Data modeling |
| Pivot Tables | Data aggregation |
| Excel Charts | Dashboard visualization |

---

## Data Analysis Workflow

The project follows a structured data analytics workflow:

Data Extraction
↓
Data Cleaning
↓
Data Transformation
↓
Data Modeling
↓
Data Analysis
↓
Dashboard Creation
↓
Executive Summary

---

## Data Cleaning

Data cleaning was performed using **Power Query**.

Steps performed:

- Removed unnecessary columns such as product descriptions.
- Corrected incorrect data types.
- Converted numeric customer identifiers into **text format** for readability.
- Ensured **Price (INR)** was formatted as currency.

---

## Data Transformation

Several derived columns were created to enable deeper analysis.

| New Column | Description |
|------------|------------|
| Month [Order_Date] | Extracted month from order date for monthly analysis |
| Hour [Order_Time] | Extracted hour from order time |
| Hour [Delivery_Time] | Extracted hour from delivery time |
| Diff_Order_Delivery | Difference between delivery date and order date (days) |
| Day Name | Day of the week extracted from order date |

---

## Data Enrichment

The **Orders table did not contain product price**, so a **Left Join** was performed between:
Orders → Products
using **Product ID** to bring the **Price column** into the Orders table.

---

## Data Modeling

A **Star Schema** was implemented using **Power Pivot**.

Fact Table:
Orders

Dimension Tables:
Customers
Products

Relationships were created using:
Customer ID
Product ID

This model allows efficient analysis across multiple tables using pivot tables.

---

## Calculated Fields

### Revenue

A calculated column was created in the Orders table:
Revenue = Price × Quantity

This metric was used to calculate revenue-related KPIs.

---

## Business Questions Answered

This analysis answers the following business questions:

1. Total Revenue generated
2. Average Order and Delivery Time
3. Monthly Sales Performance
4. Top Products by Revenue
5. Average Customer Spending
6. Sales Performance by Top Products
7. Top 10 Cities by Number of Orders
8. Relationship between Order Quantity and Delivery Time
9. Revenue comparison between occasions
10. Product popularity by occasion

---

## Dashboard

The final dashboard provides a visual overview of key metrics and trends.

Features included:

- KPI cards for Total Orders, Revenue, Average Delivery Time, and Average Customer Spend
- Revenue by Occasion
- Revenue by Category
- Revenue by Hour
- Monthly Revenue Trends
- Top 5 Products by Revenue
- Top 10 Cities by Orders
- Interactive slicers for filtering

<img width="1878" height="852" alt="FNP Dashboard" src="https://github.com/user-attachments/assets/de126d22-efdd-484a-811f-a36bae739120" />

---

## Key Insights

- Certain occasions such as **Anniversaries and Raksha Bandhan generate higher revenue**.
- The **Colors category contributes the largest share of revenue**.
- Sales show **seasonal spikes during festive periods**.
- Some cities contribute significantly more orders than others.
- Correlation between **order quantity and delivery time is nearly zero**, indicating order size does not impact delivery efficiency.

---

## Executive Summary

This project analyzes sales data from Ferns & Petals (FNP), a gifting platform that delivers products for various occasions such as birthdays, anniversaries, and major festivals. The objective of the analysis was to explore sales trends, evaluate operational efficiency, and identify key drivers of revenue to support business decision-making.

Using Excel's Power Query and Power Pivot capabilities, the dataset was cleaned, transformed, and structured into a relational data model. Additional analytical features such as monthly trends, hourly order patterns, and delivery duration were derived to enable deeper insights. A star schema model was implemented with Orders as the central fact table connected to product and customer dimensions, allowing efficient multi-dimensional analysis.

The analysis revealed that revenue is strongly influenced by seasonal occasions, with events like anniversaries and Raksha Bandhan contributing significantly to overall sales. Product categories such as decorative and gift-related items represent major revenue drivers, indicating strong customer demand for themed gifting products.

Customer purchasing behavior shows an average spending value of approximately ₹3,520 per order, while the average delivery time of about 5.5 days indicates stable operational performance. Correlation analysis between order quantity and delivery duration showed almost no relationship, suggesting that larger orders do not negatively impact delivery timelines.

Overall, the dashboard provides a clear view of FNP’s sales performance and enables stakeholders to make **data-driven decisions related to marketing strategy, product offerings, and operational efficiency**.
