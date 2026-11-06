# Customer Shopping Behavior Analysis

This project analyzes customer shopping behavior using SQL, Python, and Power BI to uncover patterns in revenue, discounts, customer segments, product demand, and subscription impact.

## Project Overview

The objective is to understand how customers shop across categories, how discounts influence spending, which products perform best, and how customer segments differ in purchasing behavior. The analysis combines:

- Structured SQL queries for exploratory analysis
- Python-based data exploration and validation
- Power BI dashboarding for business reporting

## Dataset

The project uses a customer shopping dataset with 3,900 records and includes the following fields:

- Customer ID
- Age
- Gender
- Item Purchased
- Category
- Purchase Amount (USD)
- Location
- Size
- Color
- Season
- Review Rating
- Subscription Status
- Shipping Type
- Discount Applied
- Promo Code Used
- Previous Purchases
- Payment Method
- Frequency of Purchases

## Repository Contents

- `customer_shopping_behavior.csv` — source dataset used for analysis
- `customer_behavior_sql_queries.sql` — SQL queries covering business questions and analytical insights
- `Customer_Shopping_Behavior_Analysis.ipynb` — Python notebook with exploratory analysis and data processing
- `customer_behavior_dashboard.pbix` — Power BI dashboard for visual storytelling
- `Customer-Shopping-Behavior-Analysis.pptx` — presentation deck summarizing findings
- `Customer Shopping Behavior Analysis.pdf` — PDF version of the presentation
- `Business Problem  Document.pdf` — business problem statement and context

## Business Questions Answered

The SQL analysis covers key questions such as:

1. Total revenue by gender
2. Customers who used discounts and still spent above average
3. Top 5 products by average review rating
4. Average purchase amount by shipping type
5. Spending comparison between subscribers and non-subscribers
6. Products with the highest discount usage rate
7. Customer segmentation into New, Returning, and Loyal groups
8. Top 3 products per category by order count
9. Relationship between repeat purchases and subscription status
10. Revenue contribution by age group

## Tools and Technologies

- SQL: PostgreSQL-style queries for aggregations and segmentation
- Python: Pandas and Jupyter for data exploration and validation
- Power BI: Dashboard and KPI reporting
- Excel-style business reporting and presentation materials

## Workflow

1. Load the customer shopping dataset into a SQL environment or Python workflow.
2. Explore data quality, missing values, and high-level metrics.
3. Run business logic queries for customer behavior insights.
4. Validate findings using Python analysis.
5. Build visual dashboards in Power BI.
6. Communicate results through presentation materials.

## Suggested Usage

### SQL analysis
Open `customer_behavior_sql_queries.sql` in a SQL client and execute queries to replicate the core analysis.

### Python exploration
Open `Customer_Shopping_Behavior_Analysis.ipynb` in Jupyter Notebook or VS Code to inspect data trends and validate the results.

### Power BI dashboard
Open `customer_behavior_dashboard.pbix` in Power BI Desktop to view the interactive dashboard.

## Key Insights (Example)

The project is designed to highlight insights such as:

- Whether male or female customers generate more revenue
- The impact of discounts on customer spending
- Which items are most valued by rating and demand
- How shipping speed affects average spend
- Whether subscription members spend more than non-members
- Customer loyalty patterns and repeat purchase behavior

## Getting Started

1. Download or clone the repository.
2. Ensure you have access to:
   - Python and Jupyter Notebook
   - A SQL environment or client
   - Power BI Desktop
3. Review the SQL queries and notebook to understand the analysis flow.
4. Open the dashboard for presentation-ready visuals.

## Notes

This project is useful for hands-on learning in:

- Data analysis
- SQL querying
- Business intelligence
- Customer analytics
- Dashboard design

## License

This repository is intended for educational and portfolio use. Please review any project-specific restrictions before commercial reuse.
