# 📊 Shopify App Store Analysis – Power BI Project

## 📝 Project Overview

In this Power BI project, I analyzed public data scraped from the Shopify App Store to identify what makes an app successful. The goal was to understand the app landscape, evaluate user reviews, and assess developer responsiveness. This project was completed as part of the TripleTen Business Intelligence Analyst Bootcamp.

---

## 📚 Table of Contents

1. [Project Objective](#1-project-objective)
2. [Dataset Overview](#2-dataset-overview)
3. [Tools & Technologies](#3-tools--technologies)
4. [Power BI Report Structure](#4-power-bi-report-structure)
5. [Key Metrics & Visuals](#5-key-metrics--visuals)
6. [Insights & Interpretations](#6-insights--interpretations)
7. [Conclusion](#7-conclusion)
8. [Future Enhancements](#8-future-enhancements)
9. [Getting Started](#9-getting-started)

---

## 1. 🎯 Project Objective

- Explore the types of apps available in the Shopify App Store.
- Understand how user reviews and helpfulness ratings relate to app success.
- Assess how developer responsiveness affects user satisfaction.
- Identify the most impactful developers and apps by review quality, not just quantity.

---

## 2. 📂 Dataset Overview

- **File**: `shopify.xlsx`
- **Source**: Provided by [TripleTen](https://tripleten.com/) as part of their Business Intelligence Analyst program
- **Download Raw Data**: [Click here to access the dataset](https://practicum-content.s3.us-west-1.amazonaws.com/data-eng/BIA/Dataset/shopify.xlsx)
- **Tables Included**:
  - `apps`: App details (name, developer, ratings, review count, etc.)
  - `apps_categories`: Many-to-many join table between apps and categories
  - `categories`: List of app categories
  - `reviews`: User reviews including rating, comment, helpful count, and developer replies


---

## 3. 🛠 Tools & Technologies

- **Power BI Desktop**: For data modeling and dashboard creation
- **DAX**: For creating custom columns and measures
- **Excel**: For minor pre-processing
- **Relationship Modeling**: To link reviews with apps for aggregated analysis

---

## 4. 🧭 Power BI Report Structure

The Power BI file contains three main pages:

### 🔹 App Landscape
- Total unique apps (KPI card)
- Line chart of review count over time (`lastmod`)
- Scatterplot of average rating vs number of reviews

### 🔹 Reviews
- DAX column `helpful_reviews = rating * (1 + helpful_count)`
- Card showing average helpful review score
- DAX column `developer_answered = IF(ISBLANK(developer_reply), 0, 1)`
- Scatterplot: developer_answered (X) vs average rating (Y)

### 🔹 App Reviews
- Relationships built:
  - `reviews[app_id]` → `apps[id]`
- Bar chart: Developer vs Total Rating
- Bar chart: Developer vs Average Helpful Review Score
- Bar chart: Most responsive developers (Developer vs Avg `developer_answered`), filtered to apps with more than 500 reviews

---

## 5. 📈 Key Metrics & Visuals

| Page | Visual | Description |
|------|--------|-------------|
| App Landscape | KPI Card | Total unique apps on the platform |
| App Landscape | Line Chart | Sum of reviews over time |
| App Landscape | Scatterplot | Ratings vs Number of Reviews |
| Reviews | Card | Avg. weighted helpful review score |
| Reviews | Scatterplot | Developer responsiveness vs average rating |
| App Reviews | Bar Charts | Top developers by rating, helpfulness, and responsiveness |

---

## 6. 💡 Insights & Interpretations

- 📈 Apps with higher helpful reviews tend to receive more consistent positive feedback.
- ⏱ Developer responsiveness (responding to reviews) positively correlates with higher average ratings.
- 🔝 Some developers dominate in terms of total ratings, but when weighted by helpfulness, other high-quality contributors stand out.
- 🆓 Freemium apps attract more reviews, which may impact visibility and perception.

---

## 7. ✅ Conclusion

This analysis provides a foundation for understanding how review quality, responsiveness, and category placement affect app success in the Shopify ecosystem. For developers and product teams, the most actionable insight is to focus on **engaging with users** and maintaining app quality through **active support**.

---

## 8. 🚀 Future Enhancements

- Sentiment analysis on review comments
- Merge with app install/download data if available
- Interactive filters by app category and pricing model
- Time-series trends on responsiveness vs ratings

---

## 9. 💻 Getting Started

To explore the project:

1. Open `shopify_app.pbix` in Power BI Desktop.
2. Ensure the original `shopify.xlsx` dataset is placed in the same directory.
3. Navigate to the three report tabs: `App Landscape`, `Reviews`, `App Reviews`.
4. Interact with slicers and visuals to explore insights dynamically.

---

## 🙋‍♀️ About the Author

**Pema Gurung**  
Business Intelligence Analyst | Excel • SQL • Power BI • Tableau
📧 pemagrg916@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/pema-gurung)

---

> ⭐ If you found this project insightful, feel free to star the repository and connect with me on LinkedIn!
