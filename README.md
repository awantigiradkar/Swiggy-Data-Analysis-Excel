# Swiggy Data Analysis Dashboard (Excel)

An interactive Excel dashboard designed to analyze restaurant order patterns, sales metrics, and customer preferences on Swiggy. The dashboard utilizes pivot tables, advanced custom number formatting, and interactive slicers to provide a dynamic business intelligence tool.

## Dashboard Preview
<video src="Swiggy%20Data%20Analysis%20Video.mp4" width="100%" controls autoplay loop muted></video> 
---

## Project Objectives
The goal of this project was to analyze Swiggy order transactions and extract actionable insights for restaurant partners and platform optimization:
1. **Sales Performance:** Track overall revenue (`Total Sales`), order volume (`Total Orders`), and average metrics (`AOV` and ratings).
2. **Time-Series Analysis:** Identify peaks in order volume across months, days of the week, and quarters.
3. **Geographical Performance:** Identify the highest-revenue states and top cities.
4. **Food Preferences:** Analyze sales breakdown across food categories (e.g., Veg vs. Non-Veg).
5. **Interactive Exploration:** Allow stakeholders to drill down by month, state, or restaurant name dynamically.

---

## Dataset Description
The dataset contains transaction-level raw data from Swiggy containing the following columns:
* **State:** The state where the order was placed.
* **City:** The city of the restaurant.
* **Order Date:** Transaction timestamp.
* **Restaurant Name:** The name of the restaurant.
* **Location:** Neighborhood or locality.
* **Category:** Dish category (Snacks, Recommended, Main Course, etc.).
* **Dish Name:** The name of the specific item ordered.
* **Price (INR):** The selling price of the item.
* **Rating:** The customer rating for the dish (out of 5).
* **Rating Count:** Number of reviews for the dish.

---

## Advanced Excel Features Implemented
* **Dynamic KPI Cards:** Designed high-level metric cards (`Total Sales`, `Total Orders`, `Rating Count`) linked directly to source sheets.
* **Dynamic Formatting Rules:** Implemented conditional custom formatting to automatically scale units:
  * Scales to **Millions (M)** at a global/unfiltered level (e.g., `₹ 53.01M`).
  * Scales down to **Thousands (K)** when filtered by specific restaurants or cities (e.g., `₹ 150.0K`) to maintain numerical precision.
  * **Custom Code used:** `[>=1000000]₹ #,##0.00,, "M";[>=1000]₹ #,##0.0, "K";₹ #,##0`
* **Interactive Slicers:** Connected slicers for **Months**, **Restaurant Name**, and **State** to multiple Pivot Tables and Charts to synchronize the entire dashboard.
* **Geographical Filled Maps:** Plot sales density across India to visually distinguish major state-level contributors.

---

## Key Insights Discovered
* **Top Revenue Drivers:** Maharashtra (specifically Mumbai) and West Bengal (specifically Kolkata) are the leading revenue-generating states.
* **Average Order Value (AOV):** While order volume fluctuates, the Average Order Value remains relatively stable around `₹268.51`, highlighting a consistent ticket size per transaction.
* **Weekday vs. Weekend Splitting:** Orders show a significant surge on weekends (Saturday & Sunday), indicating higher recreational demand.
* **Food Type Preference:** Veg options dominate total order count in several regions, suggesting a larger target market segment for vegetarian menus in Swiggy's database.
