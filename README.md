# 🛒 Zepto E-Commerce SQL Data Analysis Project  

A complete end-to-end **SQL Data Analyst portfolio project** built using an e-commerce inventory dataset inspired by **Zepto**, one of India’s fastest-growing quick-commerce startups.  
This project replicates real-world analyst workflows — from raw data exploration to business-focused SQL insights.  

---

## 🎯 Ideal For  
- 📊 **Aspiring Data Analysts** building a strong portfolio for interviews or LinkedIn  
- 🧠 **Learners practicing SQL hands-on** with realistic datasets  
- 💼 **Professionals preparing for roles** in retail, e-commerce, or product analytics  

---

## 📌 Project Overview  

This project simulates how data analysts in the e-commerce industry use SQL to:

✅ Create and organize a real-world inventory database  
✅ Perform **Exploratory Data Analysis (EDA)** to study product categories and stock levels  
✅ Clean messy data (handle nulls, invalid values, and convert paise to rupees)  
✅ Derive **business insights** using SQL queries for pricing, revenue, and inventory optimization  

---

## 📁 Dataset Overview  

The dataset (originally scraped from Zepto’s product listings and available on Kaggle) closely mirrors real e-commerce catalog data.  
Each record represents a **unique SKU (Stock Keeping Unit)** — products may appear multiple times with variations in weight, discounts, or packaging.  

### 🧾 Columns  

| Column | Description |
|---------|-------------|
| `sku_id` | Unique product identifier (Primary Key) |
| `name` | Product name as shown on the app |
| `category` | Product category (e.g., Fruits, Snacks, Beverages) |
| `mrp` | Maximum Retail Price (converted from paise to ₹) |
| `discountPercent` | Discount applied on MRP |
| `discountedSellingPrice` | Final selling price after discount |
| `availableQuantity` | Units available in inventory |
| `weightInGms` | Product weight in grams |
| `outOfStock` | Boolean flag for stock availability |
| `quantity` | Number of units per package or loose produce |

---

## 🔧 Project Workflow  

### 1️⃣ Database & Table Creation  

```sql
CREATE TABLE zepto (
  sku_id SERIAL PRIMARY KEY,
  category VARCHAR(120),
  name VARCHAR(150) NOT NULL,
  mrp NUMERIC(8,2),
  discountPercent NUMERIC(5,2),
  availableQuantity INTEGER,
  discountedSellingPrice NUMERIC(8,2),
  weightInGms INTEGER,
  outOfStock BOOLEAN,
  quantity INTEGER
);
