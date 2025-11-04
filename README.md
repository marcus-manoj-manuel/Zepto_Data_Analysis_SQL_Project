# 🛒 Zepto Data Analysis SQL Project  

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
```

---

### 2️⃣ Data Import  

Loaded the CSV file into PostgreSQL using **pgAdmin’s Import Tool**.  
If import fails (encoding issue), use:

```sql
\copy zepto(category,name,mrp,discountPercent,availableQuantity,
discountedSellingPrice,weightInGms,outOfStock,quantity)
FROM 'data/zepto_v2.csv' WITH (FORMAT csv, HEADER true, DELIMITER ',', QUOTE '"', ENCODING 'UTF8');
```

If UTF-8 errors occur, re-save the file as **CSV UTF-8**.

---

### 3️⃣ 🔍 Data Exploration  

- Counted total records in the dataset  
- Previewed sample rows to understand structure  
- Checked for null and duplicate values  
- Extracted unique product categories  
- Compared in-stock vs out-of-stock items  
- Identified duplicate SKUs for the same products  

---

### 4️⃣ 🧹 Data Cleaning  

- Removed rows where MRP or discounted price equals 0  
- Converted prices from paise to rupees for clarity  
- Standardized inconsistent column data  

---

### 5️⃣ 📊 Business Insights (SQL Queries)  

- Found **Top 10 best-value products** based on discount percentage  
- Identified **high-MRP products** currently out of stock  
- Estimated **potential revenue per category**  
- Filtered **expensive items (MRP > ₹500)** with low discounts  
- Ranked **top 5 categories** by average discount  
- Calculated **price per gram** for best-value identification  
- Grouped products into **Low / Medium / Bulk** weight segments  
- Summed **total inventory weight per category**  

---

## 🛠️ How to Run the Project  

```bash
# Clone the repository
git clone https://github.com/marcus-manoj-manuel/Zepto_Data_Analysis_SQL_Project.git

# Navigate into the project folder
cd Zepto_Data_Analysis_SQL_Project
```

1. Open the `zepto.sql` file  
   – Includes table creation, EDA, cleaning, and business analysis queries  
2. Import the dataset (`data/zepto_v2.csv`) — ensure it’s saved as UTF-8  
3. Run the SQL file inside **pgAdmin** or any PostgreSQL client  
4. Follow along with the YouTube walkthrough 👨‍💼  

---

## 📜 License  

This project is licensed under the **MIT License**.  
Feel free to fork, star ⭐, and use it in your portfolio.  

---

## 👨‍💻 Author  

**Marcus Manoj Manuel**  
🎓 Data Analyst | SQL | Power BI | Python | Data Storytelling  

🔗 [LinkedIn Profile](https://www.linkedin.com/in/marcus-manoj-manuel-a489642a9/)  

Let’s connect and grow in the data journey together 🚀
