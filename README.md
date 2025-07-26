# ❄️ Snowflake Data Warehouse Project – SleekMart OMS

A fully structured **Snowflake Data Warehouse** implementation built using Snowflake SQL, dimensional modeling, and scalable table design.

## 📌 Project Overview

This project simulates a retail company's **Order Management System (OMS)** using a Snowflake data warehouse. It covers a full pipeline from raw data ingestion to structured fact table creation for regional sales analysis.

## 🧱 Architecture

![Architecture](architecture.png)

 **Landing Layer (`L1_LANDING`)**: Contains raw but structured transactional data.
 **Training Layer (`TRAINING`)**: Contains transformed regional sales fact tables.
 **UPDATED_AT** fields are used for change tracking.

## 📂 Schemas & Tables

### 🔹 `L1_LANDING` Schema
- `CUSTOMERS`
- `PRODUCTS`
- `DATES`
- `STORES`
- `EMPLOYEES`
- `SUPPLIERS`
- `ORDERS`
- `ORDERITEMS`

### 🔹 `TRAINING` Schema
- `SALES_US`
- `SALES_UK`
- `SALES_INDIA`

---

## 🧪 Key Features

- ✅ Clean dimensional modeling
- ✅ Region-wise fact tables
- ✅ Use of `UPDATED_AT` for tracking
- ✅ Fully built with Snowflake SQL
- ✅ Insert scripts for real sample data

---

## ⚙️ How It Works

1. **Create schemas and landing tables** using `CREATE TABLE` statements.
2. **Insert data** using provided `INSERT INTO` SQL scripts.
3. **Transform and load** data into regional fact tables:
   - Join `ORDERS`, `ORDERITEMS`, `PRODUCTS`, `CUSTOMERS`, and `STORES`.
   - Filter based on `STATE` (e.g., `'TX'`, `'CA'`, `'NY'` → US).
4. **Query fact tables** for insights like sales amount, customer activity, etc.
