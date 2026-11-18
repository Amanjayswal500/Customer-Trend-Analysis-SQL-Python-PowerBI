# Customer Shopping Behavior Analysis

<p align="center">
  <img src="https://img.shields.io/badge/SQL-Business%20Analysis-336791?logo=postgresql&logoColor=white" alt="SQL">
  <img src="https://img.shields.io/badge/Python-Data%20Analysis-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black" alt="Power BI">
  <img src="https://img.shields.io/badge/Status-Completed-green" alt="Status">
</p>

<p align="center">
  <strong>A SQL, Python, and Power BI portfolio project analyzing customer shopping behavior, purchasing patterns, discounts, subscriptions, product demand, and customer segments.</strong>
  <br>
  The project uses 3,900 customer records to uncover actionable retail and marketing insights.
</p>

---

## Table of Contents

- [About This Project](#about-this-project)
- [Problem Statement](#problem-statement)
- [Business Questions](#business-questions)
- [Dataset Overview](#dataset-overview)
- [Project Structure](#project-structure)
- [Methodology](#methodology)
  - [1. Data Preparation](#1-data-preparation)
  - [2. SQL Analysis](#2-sql-analysis)
  - [3. Python Analysis](#3-python-analysis)
  - [4. Power BI Dashboard](#4-power-bi-dashboard)
- [Key Findings](#key-findings)
- [Business Recommendations](#business-recommendations)
- [Technical Specifications](#technical-specifications)
- [How to Review the Project](#how-to-review-the-project)
- [Limitations](#limitations)
- [Author](#author)

---

## About This Project

This project analyzes customer purchasing behavior using a single transaction-level shopping dataset. SQL is used for structured business queries, Python is used for exploratory analysis and validation, and Power BI is used to present interactive business insights.

The analysis focuses on:

- Revenue and purchase patterns by customer demographics
- Product category and item-level performance
- Discount and promotion usage
- Subscription and loyalty behavior
- Shipping preferences and purchase frequency
- Regional, seasonal, and age-group trends

The project demonstrates:

- **SQL analysis:** Filtering, aggregation, window functions, segmentation, and ranking.
- **Python analysis:** Data loading, profiling, cleaning validation, and exploratory analysis.
- **Business analysis:** Translating retail patterns into evidence-based recommendations.
- **Power BI reporting:** Building an interactive dashboard with KPIs and demographic, product, and behavior comparisons.

---

## Problem Statement

Customer purchasing activity varies across gender, age, geography, product category, subscription status, shipping method, season, and discount usage. Examining only one metric can hide differences in average spend, revenue contribution, and customer loyalty.

This project uses transaction-level customer data to identify high-performing segments and products and to evaluate how promotions and subscriptions relate to purchasing behavior.

---

## Business Questions

1. **Revenue by customer:** What is the total and average revenue by gender and age group?
2. **Discount behavior:** Which customers use discounts while spending at or above the average purchase amount?
3. **Product ratings:** Which products have the highest average customer review ratings?
4. **Shipping behavior:** How do average purchase amounts differ across shipping types?
5. **Subscriptions:** Do subscribed customers generate more revenue or spend more per order?
6. **Discount concentration:** Which products have the highest discount usage rates?
7. **Customer segmentation:** How many customers are New, Returning, or Loyal based on previous purchases?
8. **Category performance:** What are the top three most-purchased products within each category?
9. **Repeat buyers:** Are repeat buyers more likely to have a subscription?
10. **Age contribution:** Which age groups contribute the most revenue?

---

## Dataset Overview

The project uses one source CSV file containing 3,900 customer records.

| Dataset | Description |
|---|---|
| `Dataset/customer_shopping_behavior.csv` | Customer-level shopping transactions and attributes |

### Dataset Summary

| Attribute | Details |
|---|---:|
| Customer records | 3,900 |
| Unique customers | 3,900 |
| Data fields | 18 |
| Unique locations | 50 |
| Product items | 25 |
| Product categories | 4 |
| Source format | CSV |
| Missing values | 37 missing review ratings |

The data includes purchase amount, item, category, location, season, size, color, review rating, subscription status, shipping type, discount status, payment method, previous purchases, and purchase frequency.

---

## Project Structure

```text
Customer-Trend-Analysis-SQL-Python-PowerBI/
│
├── Dataset/
│   └── customer_shopping_behavior.csv
│
├── sql/
│   └── customer_behavior_sql_queries.sql
│
├── notebooks/
│   └── Customer_Shopping_Behavior_Analysis.ipynb
│
├── powerbi/
│   └── customer_behavior_dashboard.pbix
│
├── reports/
│   ├── Customer-Shopping-Behavior-Analysis.pptx
│   ├── Customer Shopping Behavior Analysis.pdf
│   └── Business Problem  Document.pdf
│
├── LICENSE
└── README.md
```

---

## Methodology

### 1. Data Preparation

The source dataset was profiled for record count, missing values, unique values, data types, and inconsistencies. The 37 missing review ratings are retained as missing values rather than replacing them with a potentially misleading estimate.

The analysis preserves the customer-level grain and uses fields directly relevant to the defined business questions.

### 2. SQL Analysis

The SQL script in `sql/customer_behavior_sql_queries.sql` contains 10 analytical queries covering:

| Query | Purpose |
|---|---|
| Q1 | Revenue by gender |
| Q2 | Discount users spending above the average |
| Q3 | Top products by review rating |
| Q4 | Average purchase amount by shipping type |
| Q5 | Subscription status and customer spending |
| Q6 | Products with the highest discount usage |
| Q7 | New, Returning, and Loyal customer segmentation |
| Q8 | Top three products within each category |
| Q9 | Repeat-buyer subscription relationship |
| Q10 | Revenue by age group |

The segmentation logic classifies customers with 1 previous purchase as New, 2–10 as Returning, and more than 10 as Loyal.

### 3. Python Analysis

The Jupyter notebook performs exploratory data analysis and validates the data used for SQL and reporting. Typical checks include:

- Dataset shape and schema
- Missing and unique values
- Summary statistics
- Revenue, product, category, shipping, and segment comparisons
- Review of relationships between customer attributes and purchase amounts

### 4. Power BI Dashboard

The Power BI dashboard provides interactive views of customer spending and shopping behavior. Open `powerbi/customer_behavior_dashboard.pbix` in Microsoft Power BI Desktop to review the report and refresh or update the source if the local data path changes.

The dashboard is designed to compare customer segments, revenue, products, and purchasing patterns together rather than relying on a single metric.

---

## Key Findings

### 1. Revenue and Customer Composition

- The dataset contains **3,900 customers** and **$233,081** in total purchase amount.
- Male customers account for **$157,890** in revenue, compared with **$75,191** from female customers.
- Average purchase amount is **$59.76** overall and is nearly equal across genders: **$59.54** for male and **$60.25** for female customers.
- Male customers represent 68% of the records, while female customers represent 32%.

**Interpretation:** Male customers generate more total revenue primarily because there are more male records, not because their average transaction is substantially larger.

### 2. Product and Category Performance

- Clothing is the largest category at **$104,264** in revenue, followed by Accessories at **$74,200**, Footwear at **$36,093**, and Outerwear at **$18,524**.
- Clothing accounts for approximately **44.74%** of total revenue.
- The highest-revenue individual products include Blouse (**$10,410**), Shirt (**$10,332**), Dress (**$10,320**), and Pants (**$10,090**).
- Gloves have the highest average review rating at **3.86**, followed by Sandals (**3.84**) and Boots (**3.82**).
- The overall average review rating is **3.75**.

**Interpretation:** Revenue is concentrated in Clothing and a small set of high-volume items. Product ratings should be considered separately from sales value.

### 3. Discount Behavior

- **43%** of purchases used a discount.
- Purchases with discounts have a slightly lower average amount: **$59.28**, compared with **$60.13** for purchases without discounts.
- **839 customers** used a discount and spent at least the overall average purchase amount.
- Hats have the highest discount usage rate at **50.00%**, followed by Sneakers (**49.66%**) and Coats (**49.07%**).

**Interpretation:** Discounts are widely used, but they are not associated with a higher average purchase amount in this dataset.

### 4. Subscription and Loyalty

- Only **27%** of customers are subscribed.
- Subscribed customers have an average purchase amount of **$59.49** and non-subscribed customers have **$59.87**.
- Non-subscribers contribute **$170,436** in total revenue; subscribers contribute **$62,645**.
- The segment distribution is **83 New**, **701 Returning**, and **3,116 Loyal** customers.
- Among customers with more than five previous purchases, 2,518 are non-subscribed and 958 are subscribed.

**Interpretation:** Subscription status does not correspond to higher average spend, and subscription conversion is an opportunity for an otherwise loyal customer base.

### 5. Shipping, Season, and Geography

- Express shipping averages **$60.48** per purchase, compared with **$58.46** for Standard shipping.
- Fall is the strongest season by purchase value at **$60,018**, followed by Spring at **$58,679**.
- Montana is the highest-revenue location at **$5,784**; Illinois follows at **$5,617**.
- The 55+ age group contributes the most revenue at **$69,590**.

**Interpretation:** Shipping speed and season show modest differences. The 55+ age group is the largest revenue contributor, while location-level results are relatively distributed across many states.

### Overall KPI Summary

| Metric | Result |
|---|---:|
| Unique customers | 3,900 |
| Total purchase amount | $233,081 |
| Average purchase amount | $59.76 |
| Average review rating | 3.75 |
| Discount purchase rate | 43% |
| Subscription rate | 27% |
| Highest-revenue category | Clothing — $104,264 |

---

## Business Recommendations

1. **Target loyal customers with subscriptions:** The customer base is heavily Loyal, but only 27% are subscribed. Subscription benefits should be promoted to high-frequency buyers.
2. **Improve discount efficiency:** Discounts are used in 43% of purchases but do not increase average spend. Test offers based on purchase thresholds, categories, or customer segments.
3. **Protect core category demand:** Clothing generates nearly 45% of revenue. Maintain availability and promote strong products such as Blouses, Shirts, Dresses, and Pants.
4. **Use ratings and revenue together:** Well-rated products can support merchandising and cross-selling decisions, even if they are not currently the highest-revenue items.
5. **Build age-specific campaigns:** The 55+ group is the largest revenue contributor, while the 25–34 and 45–54 groups are also substantial contributors.

These recommendations describe patterns in the supplied dataset and should be validated with profitability and campaign cost data before implementation.

---

## Technical Specifications

| Component | Technology / Approach |
|---|---|
| Data input | CSV |
| Data analysis | SQL and Python |
| SQL style | PostgreSQL-compatible |
| Python libraries | Pandas and Jupyter |
| Dashboard | Microsoft Power BI |
| Reporting | PBIX, PDF, and PPTX |
| Analysis type | Descriptive and exploratory customer analytics |

---

## How to Review the Project

### 1. Review the Source Data

Open `Dataset/customer_shopping_behavior.csv` to inspect the 18 source fields and 3,900 customer records.

### 2. Review the SQL Analysis

Open `sql/customer_behavior_sql_queries.sql` in a compatible SQL environment and execute the queries.

The script is written for PostgreSQL-style syntax, including `::numeric`, `LIMIT`, and window functions.

### 3. Review the Python Notebook

Open `notebooks/Customer_Shopping_Behavior_Analysis.ipynb` in Jupyter Notebook or VS Code. Install the required Python packages if they are not already available.

### 4. Open the Power BI Dashboard

Open `powerbi/customer_behavior_dashboard.pbix` in Microsoft Power BI Desktop.

If the source path is not resolved automatically, update the data source to point to `Dataset/customer_shopping_behavior.csv`, then refresh the report.

### 5. Review the Reports

Presentation and business problem documents are available in `reports/`:

- `Customer-Shopping-Behavior-Analysis.pptx`
- `Customer Shopping Behavior Analysis.pdf`
- `Business Problem  Document.pdf`

---

## Limitations

- **No purchase-date field:** A true monthly or yearly time trend cannot be calculated from the available data.
- **No transaction quantity or cost:** Purchase amount is used instead of unit quantity, profit, or cost of goods sold.
- **Missing ratings:** 37 review-rating values are missing.
- **Cross-sectional evidence:** Findings describe relationships in the supplied dataset and do not establish causality.
- **Subscription and discount outcomes:** The dataset does not include campaign cost, incremental revenue, or profitability.
- **External validation:** The repository does not include external demographic or market reference data.

---

## Author

**Aman Jayswal**

- GitHub: [@Amanjayswal500](https://github.com/Amanjayswal500)
- Repository: [Customer-Trend-Analysis-SQL-Python-PowerBI](https://github.com/Amanjayswal500/Customer-Trend-Analysis-SQL-Python-PowerBI)

<p align="center">
  <strong>Customer Shopping Behavior Analysis</strong>
  <br>
  SQL • Python • Power BI • Customer Analytics
</p>
