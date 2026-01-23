# Zomato Data Analysis: Customer Segmentation & Strategic Insights

## 📌 Project Overview
The goal of this project was to analyze Zomato’s customer base to identify key demographic drivers and purchasing behaviors. By leveraging **Power BI**, I transformed raw consumer data into a strategic dashboard that identifies high-value segments and provides actionable recommendations to optimize Zomato’s marketing and operational efficiency.

## 🎯 Project Goals
* **Identify Core Demographics:** Determine the primary user base in terms of age, occupation, and income.
* **Analyze Purchasing Patterns:** Correlate family size and education levels with order quantity and value.
* **Market Segmentation:** Use machine learning (**K-Means Clustering**) to group customers into "High-Value," "Frequent," and "Budget" tiers.
* **Drive Revenue Growth:** Provide data-backed recommendations for targeted marketing and partnership opportunities.

## 🛠️ Data Preparation & Cleaning
I performed extensive data preprocessing in **Power Query** to ensure the integrity of the insights:
* **Data Type Standardization:** Converted `rating` and `cost` from text to numeric formats to enable calculations for Average Order Value (AOV).
* **Null Value Management:** Filtered out null restaurant names and incomplete demographic rows to prevent skewed percentages.
* **Feature Engineering:** * Created a **Day Type** column (Weekday vs. Weekend) using DAX: `Day of Week = FORMAT('orders'[order_date], "dddd")`.
* **Clustering Logic:** Applied K-Means clustering to normalized variables (Frequency vs. Revenue) to ensure spend amounts didn't disproportionately outweigh order counts.

## 💡 Hypotheses & Key Observations

### Hypothesis 1: The "Youth Volume" Play
> *"Zomato’s market penetration is concentrated in Gen-Z users, creating a high-volume but low-immediate-margin user base."*
* **Observation:** Users aged **18-25 (Gen Z)** represent over 70% of the platform's traffic. While they drive the highest volume, they primarily fall into the "No Income" (Student) bracket.
* **Metric:** 72% of total orders are attributed to the Student segment.

### Hypothesis 2: Household Optimization
> *"Larger households optimize for delivery costs by increasing the quantity of items per transaction."*
* **Observation:** A direct linear correlation exists between family size and **Avg Quantity per Order**. Families of 4-6 members order significantly more items per transaction than individuals.
* **Metric:** Households of 5+ members show a 2.4x higher quantity-per-order than single-member households.

### Hypothesis 3: The Value-Frequency Inverse
> *"Higher-income customers place fewer but significantly higher-value orders compared to budget-conscious segments."*
* **Observation:** The **"High-Value" Cluster** (50k+ Income) orders 20% less frequently than students but maintains a **3x higher Average Order Value (AOV)**.
* **Metric:** High-income users prioritize quality (Continental/Italian cuisines) over discount-driven Fast Food.



## 🚀 Strategic Recommendations
1. **Zomato Rewards for Families:** Launch "Family Mega-Meal" bundles on weekends to capitalize on the high-quantity trend seen in larger households.
2. **VIP Retention:** Implement a "Premium Tier" for the High-Value cluster (Post Graduates) that offers gourmet exclusives rather than standard discounts.
3. **B2B Lunch Partnerships:** Focus on the "Employee" demographic during weekdays to fill the volume gap identified between the student-driven weekend peaks.

## ⚠️ Limitations & Bias
* **Self-Reporting Bias:** Income and education levels are self-reported, which may lead to social desirability bias.
* **Sample Representativeness:** The data is heavily skewed toward Gen Z, meaning conclusions may not apply to users aged 45+.
* **Normalization Assumption:** Clusters were defined using K-means on normalized spend/frequency; changing the weighting could alter the segment sizes.

## 📂 Tools Used
* **Power BI:** Visualization & Dashboarding
* **DAX:** Advanced Measures & Calculated Columns
* **Power Query:** ETL Processes
* **Machine Learning:** K-Means Clustering for Customer Segmentation
