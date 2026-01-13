# Shopify App Analysis

## 📌 Project Overview
This project provides a comprehensive analysis of the Shopify App Store landscape. Using scraped marketplace data, I built a multi-page Power BI report to identify the key factors that drive app success, developer responsiveness, and user satisfaction.

## 🛠️ The Data Model
The analysis is powered by four relational tables:
* **Apps:** Core details of marketplace listings.
* **Categories:** Taxonomy of app types.
* **Apps_Categories:** A join table managing the many-to-many relationship between apps and categories.
* **Reviews:** User ratings, comments, and developer responses.



---

## 📊 Report Sections

### Page 1: App Landscape
Focuses on high-level market statistics and the relationship between volume and sentiment.
* **Market Size:** KPI Card tracking the total count of unique applications.
* **Growth Trends:** A Line Chart analyzing review volume over time (`lastmod` date).
* **Quality vs. Popularity:** A Scatterplot correlating `reviews_count` against `average_rating` to identify market leaders vs. niche players.

### Page 2: Review Deep-Dive & DAX Engineering
I utilized **Data Analysis Expressions (DAX)** to create custom metrics that provide a more nuanced view of user feedback.
* **Weighted Sentiment:** Created a `helpful_reviews` column using:
  ```dax
  helpful_reviews = Reviews[rating] * (1 + Reviews[helpful_count])
