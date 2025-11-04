# Zepto_Data_Analysis_SQL_Project
🛒 Zepto E-Commerce SQL Data Analysis Project

A complete end-to-end SQL Data Analyst portfolio project built using an e-commerce inventory dataset inspired by Zepto, one of India’s fastest-growing quick-commerce startups.
This project replicates real-world analyst workflows — from raw data exploration to business-oriented SQL insights.

🎯 Ideal For

📊 Aspiring Data Analysts looking to build a portfolio project for interviews or LinkedIn

🧠 Learners practicing SQL hands-on through real data

💼 Professionals preparing for roles in retail, e-commerce, or product analytics

📌 Project Overview

This project simulates the daily workflow of data analysts in the e-commerce industry using SQL to:

✅ Create and organize a real-world inventory database
✅ Perform Exploratory Data Analysis (EDA) to study products, categories, and stock levels
✅ Clean messy data — handle nulls, invalid prices, and convert paise to rupees
✅ Derive business insights through SQL queries focused on pricing, revenue, and availability

📁 Dataset Overview

The dataset (originally scraped from Zepto’s product listings and hosted on Kaggle) mirrors real e-commerce catalog data.
Each record represents a unique SKU (Stock Keeping Unit), with duplicate product names due to different sizes, discounts, or packaging variations — just like real inventory systems.

🧾 Columns
Column	Description
sku_id	Unique product identifier (Primary Key)
name	Product name as listed on the app
category	Product category (e.g., Fruits, Snacks, Beverages)
mrp	Maximum Retail Price (converted from paise to ₹)
discountPercent	Discount applied on MRP
discountedSellingPrice	Final selling price after discount
availableQuantity	Units currently available
weightInGms	Product weight in grams
outOfStock	Boolean indicator for stock status
quantity	Quantity per package or unit
