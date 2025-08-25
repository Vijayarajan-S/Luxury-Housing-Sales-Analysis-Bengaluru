
# Luxury Housing Sales Analysis - Bengaluru

This project analyzes luxury housing sales in Bengaluru using **Python**, **SQL**, and **Power BI**. It covers data cleaning, feature engineering, database insertion, and interactive dashboard creation for insights on market trends, builder performance, and buyer behavior.

---

## 🐍 Step 1: Python — Data Cleaning & Feature Engineering
- Load the raw `.csv` file containing property transactions.
- Clean inconsistent formats (e.g., `Ticket_Price_Cr`).
- Handle null values in columns like `Amenity_Score` and `Booking_Status`.
- Normalize text fields (`Builder`, `Micro_Market`, etc.).
- Derive additional columns:
  - `Price_per_Sqft`
  - `Quarter_Number`
  - `Booking_Flag`
- **Output:** Cleaned CSV or DataFrame ready for database insertion.

---

## 🧠 Step 2: SQL — Load Clean Data into RDBMS
- Create appropriate SQL table schema for `property_transactions`.
- Insert cleaned data into MySQL using Python (`SQLAlchemy``).
- 
📊 Step 3: Power BI — Visualize via Direct SQL Connection
Connect Power BI to the SQL database.
Build relationships and DAX calculations.
Create interactive dashboards:
Filters by Builder, Quarter, Micro_Market
Map visuals
Booking conversion KPIs
Insights from Buyer_Comments

Power BI Visualization Questions & Approach
Market Trends
How have luxury housing bookings changed quarter by quarter across micro-markets?
Visual: Line Chart — Quarter (X-axis), Booking_Count (Y-axis), segmented by Micro_Market.

Builder Performance
Which builders have the highest total ticket sales and how do they rank in terms of average ticket size?
Visual: Bar Chart or Table — Builder, Sum(Ticket_Price_Cr), Avg(Ticket_Price_Cr).

Amenity Impact
Is there a correlation between amenity score and booking success rate?
Visual: Scatter plot — Amenity_Score vs Booking_Conversion_Rate, bubble size by Project Count.

Booking Conversion
Which micro-markets have the highest and lowest booking conversion rates?
Visual: Stacked Column Chart — Micro_Market with % Booking_Status as stacked sections.

Configuration Demand
What are the most in-demand housing configurations (e.g., 3BHK, 4BHK)?
Visual: Pie or Donut Chart — Configuration vs Booking Count.

Sales Channel Efficiency
Which sales channels contribute most to successful bookings?
Visual: 100% Stacked Column Chart — Sales_Channel vs Booking_Status distribution.

Quarterly Builder Contribution
Which builders dominate the market each quarter?
Visual: Matrix Table — Rows = Builder, Columns = Quarter, Values = Sum(Ticket_Price_Cr).

Possession Status Analysis
How does possession status affect buyer type and booking decisions?
Visual: Clustered Column Chart — Possession_Status vs Booking_Status, colored by Buyer_Type.

SalesAnalysi_ds_project/
├─ PowerBI/
│  └─ house_analysis.pbix
├─ Data/
│  └─ cleaned_property_transactions.csv
├─ Scripts/
│  └─ data_cleaning.py
├─ README.md


Author: Vijayarajan Selvam
Date: 2025



