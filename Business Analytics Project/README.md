# E-commerce Business Analytics: Funnels & Cohorts

## 📌 Project Overview
As a Junior Analyst for a growing e-commerce company, I transformed raw transaction logs into actionable business metrics. This project involves processing high-volume event data to analyze customer behavior through two primary lenses: **Conversion Funnels** and **Cohort Retention.**

## 📊 Analysis Workflow

### Part 1: Conversion Funnel Analysis
I built a three-stage conversion funnel to evaluate how effectively the website converts interest into revenue.
* **Stages:** Product View → Add to Cart → Purchase.
* **Metric:** Count of **unique users** at each stage.
* **KPIs:** Calculated total conversion rates and step-to-step drop-off rates using Pivot Tables.



### Part 2: Data Engineering & Preparation
Before performing cohort analysis, I executed a rigorous data preparation process:
* **Purchase Isolation:** Filtered 4,000+ purchase events from raw logs into a dedicated `purchase_activity` table.
* **First Purchase Mapping:** Used `VLOOKUP()` and `MIN` aggregation to identify the acquisition date for every unique customer.
* **Attribute Engineering:**
    * `event_month`: Extracted using `TEXT(date, "YYYY-MM")`.
    * `first_purchase_month`: Identified the user's "birth" month.
    * `cohort_age`: Calculated using `DATEDIF()` to track the month-lapse between acquisition and repeat purchase.

### Part 3: Cohort & Retention Analysis
I developed a retention matrix to measure customer loyalty over a 5-month period.
* **Cohort Grouping:** Grouped users into 6 monthly cohorts based on their first purchase.
* **Retention Matrix:** Calculated the percentage of unique users returning in subsequent months (Age 1 through 4).
* **Calculation Logic:** `(Users active in Month N) / (Total users in starting Cohort)`.



## 🛠️ Technical Skills Demonstrated
* **Advanced Formulas:** `VLOOKUP()`, `DATEDIF()`, `TEXT()`, and complex nested logic.
* **Data Architecture:** Transforming raw event-based logs into user-based relational tables.
* **Pivot
