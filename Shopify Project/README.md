# Shopify App Analysis

## 📌 Project Overview
This project explores the competitive landscape of the Shopify App Store using multi-table relational data. The goal was to identify the key factors that contribute to an app's success, focusing on developer responsiveness, user sentiment, and category trends.

## 🛠️ Tech Stack & Skills
* **Tool:** Power BI Desktop
* **Data Modeling:** Established Many-to-One relationships between Apps and Reviews.
* **DAX Scripting:** Created custom calculated columns for weighted review metrics and boolean logic.
* **Statistical Viz:** Scatterplots, KPI Cards, and filtered Bar Charts.

---

## 📊 Analysis Modules

### Part 1: App Landscape
This section establishes the baseline statistics for the Shopify marketplace.
* **Market Scale:** A KPI Card tracking the unique volume of apps available.
* **Growth Trends:** A Line Chart analyzing the sum of review counts over time (`lastmod` date), identifying historical periods of high user engagement.
* **Rating Correlation:** A Scatterplot comparing `reviews_count` (X) against `average_rating` (Y) to determine if higher volume typically leads to rating stabilization.



### Part 2: Review Sentiment & Developer Engagement
Advanced DAX was used to create more nuanced success metrics.
* **Weighted Sentiment:** Created the `helpful_reviews` column using DAX:
    ```dax
    helpful_reviews = Reviews[rating] * (1 + Reviews[helpful_count])
    ```
* **Responsiveness Logic:** Engineered a `developer_answered` boolean column to track whether developers engage with their users.
* **Engagement Impact:** A Scatterplot visualizing how developer replies correlate with higher average ratings, testing the hypothesis that active support improves user perception.

### Part 3: Developer Performance & Data Modeling
Leveraging a relational data model to compare developers.
* **Data Model:** Built a Many-to-One relationship between `Reviews[app_id]` and `Apps[id]`.
* **Quality vs. Quantity:** Compared "Sum of Ratings" against "Average Helpful Reviews" to identify developers who provide genuine value rather than just high-volume, low-quality apps.
* **Responsiveness Leaderboard:** A filtered Bar Chart identifying the most responsive developers (limited to those with over 500 reviews) to find the most "reliable" high-scale players in the market.



---

## 📁 Dataset Schema
The analysis is powered by four relational tables:
1.  **Apps:** Core details (ID, developer, rating, last modified).
2.  **Reviews:** Granular user feedback, ratings, and developer replies.
3.  **Categories:** Metadata for app classification.
4.  **Apps_Categories:** A join table linking apps to their respective categories.

## 💡 Key Findings
* **Responsiveness Matters:** There is a measurable trend between developers who reply to reviews and higher overall app ratings.
* **Helpfulness Weighting:** Using DAX to weigh reviews by "helpful counts" provides a much more accurate picture of app quality than simple averages.
