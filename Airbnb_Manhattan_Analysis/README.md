# 📊 Business Analytics Project: Coworking Time

## 🔍 Project Overview

This project analyzes raw event logs from an e-commerce company's website to uncover insights about user behavior, conversion performance, and customer retention. The dataset consists of individual user activities such as product views, cart openings, and purchases.

---

## 🗂 Dataset Description

**File**: `raw_user_activity` (Excel sheet)  
**Columns**:
- `user_id`: Unique identifier for each user
- `event_type`: Type of user activity (e.g., view, cart, purchase)
- `category_code`: Product category
- `brand`: Product brand
- `price`: Price of the product
- `event_date`: Date of the event (YYYY-MM-DD)

---

## 🚀 Project Components

### 1. Conversion Funnel Analysis
**Sheet**: `conversion_funnel`  
- Built a three-step funnel: **product views → cart opens → purchases**
- Used Pivot Table to count unique users per funnel stage
- Calculated:
  - **Total conversion rate** (from view to purchase)
  - **Step-by-step conversion rate** (view → cart, cart → purchase)

### 2. Purchase Activity Isolation
**Sheet**: `purchase_activity`  
- Filtered to include only purchase events  
- Added calculated columns:
  - `event_month` (e.g., 2021-03)
  - `first_purchase_month` (user's first purchase month)
  - `cohort_age` (months since first purchase)

### 3. Cohort Analysis
**Sheet**: `cohort_analysis`  
- Grouped users by `first_purchase_month` (cohorts)
- Tracked repeat purchases by `cohort_age`
- Created a matrix to display cohort sizes over time

### 4. Retention Rates
**Sheet**: `retention_rates`  
- Calculated month-over-month retention from cohort data
- Retention = users retained / cohort size at month 0
- Visualized retention decay across 5 months

---

## 📈 Executive Summary

**Sheet**: `Executive Summary`  
- High-level summary of key findings and business implications  
- Includes visual snapshots of funnel and retention rates

---

## 📋 Workbook Structure

1. `Table of Contents`
2. `Executive Summary`
3. `conversion_funnel`
4. `retention_rates`
5. `cohort_analysis`
6. `purchase_activity`
7. `first_purchase`
8. `raw_user_activity`

---

## 🛠 Tools Used

- Microsoft Excel
- Pivot Tables
- Formulas: `TEXT()`, `VLOOKUP()`, `DATEDIF()`
- Data Cleaning & Formatting

---

## 🧠 Key Insights

- Significant drop-off occurs between product views and purchases
- Retention sharply declines after the first purchase
- Most customers do not make repeat purchases beyond the first month

---

## 📌 Notes

- All calculations were performed using Excel formulas and pivot tables
- Workbook is fully documented and organized for easy navigation


