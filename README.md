# Olist E-Commerce Analytics Dashboard | Power BI

An end-to-end e-commerce analytics project using **Power BI** to analyze the performance and operations of the Olist Brazilian e-commerce marketplace. The project transforms raw transactional data into interactive dashboards to uncover insights into sales performance, customer purchasing behaviour, product performance, and delivery operations.

## 📊 Project Overview

This project explores the Olist e-commerce dataset to understand marketplace performance from both commercial and operational perspectives.

**🎬 Dashboard Preview**

<!-- Add your Power BI dashboard screenshot here -->
<!-- Example: ![Dashboard Preview](Icons/dashboard_preview.png) -->

**🎬 Interactive Dashboard:** [View Power BI Dashboard](https://app.powerbi.com/reportEmbed?reportId=e2ac5f6d-176c-4a54-b36a-3d3841f328a3&autoAuth=true&ctid=e0793d39-0939-496d-b129-198edd916feb)

The dashboard provides insights into:

- Sales and revenue performance
- Order volume and purchasing trends
- Customer behaviour and repeat purchases
- Product and category performance
- Delivery efficiency and logistics performance
- Customer satisfaction and review scores

The objective is to translate transactional data into meaningful business insights that can support data-driven decision-making.

### 📑 Table of Contents

1. [Key Business Metrics](#-key-business-metrics)
2. [Business Questions Addressed](#-business-questions-addressed)
   - [Sales & Revenue Performance](#1--sales--revenue-performance)
   - [Customer Analytics](#2--customer-analytics)
   - [Product & Category Performance](#3--product--category-performance)
   - [Delivery & Operational Performance](#4--delivery--operational-performance)
   - [Customer Satisfaction](#5--customer-satisfaction)
3. [Data Preparation & Data Modeling](#-data-preparation--data-modeling)
4. [Tools & Technologies](#️-tools--technologies)
5. [Key Learning Outcomes](#-key-learning-outcomes)
6. [Dataset Source](#-dataset-source)

## 📌 Key Business Metrics

The dashboard tracks the following performance indicators:

| Business Area | KPI | Business Definition |
|---|---|---|
| **Sales & Revenue** | Total GMV | Total product sales value, calculated using item prices |
| **Sales & Revenue** | Total Orders | Distinct count of orders |
| **Sales & Revenue** | Average Order Value (AOV) | Total GMV divided by total orders |
| **Customer Analytics** | Unique Customers | Distinct count of customer unique IDs |
| **Customer Analytics** | Repeat Customers | Customers who placed more than one order |
| **Customer Analytics** | Repeat Purchase Rate | Repeat customers divided by unique customers |
| **Customer Satisfaction** | Average Review Score | Average customer review score |
| **Delivery & Operations** | On-Time Delivery Rate | Eligible delivered orders delivered on or before the estimated delivery date |
| **Delivery & Operations** | Late Delivery Rate | Eligible delivered orders delivered after the estimated delivery date |
| **Delivery & Operations** | Average Delivery Days | Average number of days between purchase and customer delivery |

*Note: GMV is defined in this project as the sum of product prices, excluding freight charges.*

The project uses DAX measures to calculate business KPIs and support interactive analysis. Examples include:

**Total GMV**
```dax
Total GMV =
SUM(olist_order_items_dataset[price])
```

**Average Order Value**
```dax
Average Order Value =
DIVIDE(
    [Total GMV],
    [Total Orders],
    0
)
```
*The full set of measures is available in the Power BI report.*

---

## ❓ Business Questions Addressed

The analysis focuses on answering key business questions across several analytical areas.

### 1. 💰 Sales & Revenue Performance

- What is the overall gross merchandise value (GMV)?
- How many orders were placed?
- What is the average order value?
- How does sales performance vary over time?
- Which product categories contribute most to GMV?
- Which products and sellers generate the highest sales?

### 2. 👥 Customer Analytics

- How many unique customers have purchased from the platform?
- What proportion of customers make repeat purchases?
- How many customers have placed multiple orders?
- Which customer segments contribute to marketplace sales?
- What does customer purchasing behaviour reveal about retention?

### 3. 📦 Product & Category Performance

- Which product categories generate the highest revenue?
- Which products contribute most to total sales?
- How are orders and sales distributed across product categories?
- Which products and categories demonstrate stronger marketplace performance?

### 4. 🚚 Delivery & Operational Performance

- What percentage of delivered orders arrive on time?
- What percentage of delivered orders arrive late?
- What is the average delivery duration?
- Which states experience weaker delivery performance?
- How does delivery performance vary across geographical locations?

**Delivery classification:**

- On-time: Actual delivery date is on or before the estimated delivery date.
- Late: Actual delivery date is after the estimated delivery date.
- Eligible delivered orders: Delivered orders with both actual and estimated delivery dates available.

### 5. ⭐ Customer Satisfaction

- What is the average customer review score?
- How are review scores distributed?
- Are there differences in customer satisfaction across products or categories?
- What can review scores reveal about the customer experience?

---

## 🔧 Data Preparation & Data Modeling

The project involves data preparation and modeling before dashboard development.

### Data Preparation

- Imported multiple CSV datasets into Power BI.
- Reviewed missing values and duplicate records.
- Standardized data types and cleaned relevant columns.
- Handled missing product category values using an "Unknown" category.
- Prepared data for analytical reporting.

### Data Modeling

Designed relationships between the main entities:

- Orders
- Customers
- Order Items
- Products
- Sellers
- Payments
- Reviews
- Product Category Translation

The data model connects transactional and dimension tables to support cross-functional analysis and interactive filtering.

### Data Relationships

The model uses appropriate relationship cardinality and filter direction to support reliable aggregation and avoid unnecessary bidirectional filtering.

---

## 🛠️ Tools & Technologies

| Category | Tools |
|---|---|
| Data Visualization | Microsoft Power BI |
| Data Transformation | Power Query |
| Data Modeling & Calculations | DAX |
| Data Source | Olist Brazilian E-Commerce Dataset |
| Version Control | Git & GitHub |

---

## 💡 Key Learning Outcomes

Through this project, I applied practical business intelligence and data analytics techniques, including:

- Data cleaning and transformation using Power Query.
- Data modeling and relationship management.
- Developing business KPIs using DAX.
- Designing interactive dashboards for business stakeholders.
- Translating business questions into analytical requirements.
- Evaluating commercial performance and operational efficiency.

The project follows an end-to-end analytics workflow, from raw data preparation to KPI development and dashboard reporting.

---

## 📚 Dataset Source

**Olist Brazilian E-Commerce Public Dataset**

The dataset contains anonymized e-commerce transaction records, including orders, customers, products, sellers, payments, reviews, and geographical information.

Dataset: [Olist Brazilian E-Commerce Public Dataset on Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

---

⭐ Thank you for checking out this project!