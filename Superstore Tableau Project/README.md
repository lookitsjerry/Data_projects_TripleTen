
# Superstore Data Visualization: Profitability & Risk Analysis

## 📌 Project Overview
This project performs a deep dive into the "Superstore" dataset to identify drivers of profitability and operational inefficiencies. The analysis is divided into three strategic pillars: **Profit/Loss Centers**, **Advertising ROI**, and **Returns Management**.

## 📺 Project Walkthrough
For a detailed video explanation of my findings and the dashboard functionality, please click the link below:
👉 **[Watch the Project Presentation](https://lnkd.in/gPJwDBvQ)**

---

## 🔍 Analysis Breakdown

### Part 1: Profits & Losses
The goal was to identify where the Superstore is winning and where it is losing money.
* **Profit Centers:** Identified the two highest-performing dimension pairs (e.g., Sub-category + Region).
* **Loss Management:** Targeted specific products and sub-categories that consistently yield negative margins.
* **Strategic Recommendation:** Recommended the discontinuation of specific products and defined 3 "Focus" vs. 3 "Phase-out" sub-categories.



### Part 2: Advertising Optimization
I analyzed the viability of advertising spend based on seasonal and geographic profit trends.
* **Targeting:** Identified the top 3 state/month combinations for maximum impact.
* **Willingness to Pay (WTP):** Calculated advertising budgets based on a 1/5 profit-to-ad-spend ratio.
* **Visualization:** Built a time-series analysis of average profit per month for the selected states to justify seasonal ad campaigns.

### Part 3: Return Rate & Product Health
Using a `LEFT JOIN` between the Orders and Returns tables, I analyzed product quality and customer behavior.
* **Calculated Fields:** Transformed raw return data into a binary (0/1) field to calculate return rates.
* **Risk Identification:** Visualized which products and customers have the highest return rates.
* **Strategic Correlation:** Created a scatter plot of **Average Profit vs. Average Return Rate** by dimension to determine which business segments are no longer sustainable due to high overhead costs.



---

## 🛠️ Technical Skills Demonstrated
* **Data Joining:** Executed `LEFT JOINS` to merge transaction data with returns data without losing order records.
* **Calculated Fields:** Authored logic to handle null values and create custom KPIs (Return Rates, Ad-Spend Budgets).
* **Data Visualization:** Built interactive dashboards using professional grading rubrics as a standard.
* **Business Strategy:** Translated data visualizations into "Keep vs. Drop" recommendations for executive stakeholders.

## 📁 Repository Contents
* `Superstore_Analysis.twbx` (or .pbix): The primary visualization file.
* `Data_Transformations.md`: A summary of the calculated fields and join logic used.
* `Executive_Summary.pdf`: A high-level report of the 3 "Focus" sub-categories and advertising plan.

---
*This analysis provides a roadmap for the Superstore to increase net profitability by optimizing their product mix and marketing spend.*
