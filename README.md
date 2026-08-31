# Customer Shopping Behavior Analysis  
### End-to-End Data Analytics Portfolio Project | Python · SQL · Power BI

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-MySQL%20%7C%20PostgreSQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=flat&logo=powerbi&logoColor=black)
![Pandas](https://img.shields.io/badge/Pandas-EDA-150458?style=flat&logo=pandas&logoColor=white)

> A complete, industry-style retail analytics workflow — from messy raw data to executive recommendations.  
> Built exactly the way data analysts work in real organizations.

---

## Business Problem

A leading retail company wants to understand customer shopping behavior to improve sales, satisfaction, and long-term loyalty. Management has noticed shifts in purchasing patterns across demographics, product categories, and channels.

**Core question:**  
*How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?*

---

## Project Workflow

| Step | Tool             | Deliverable                               |
| ---- | ---------------- | ----------------------------------------- |
| 01   | Business framing | Problem statement & success criteria      |
| 02   | Python (pandas)  | Data cleaning, EDA, feature engineering   |
| 03   | SQL              | 10 structured business questions          |
| 04   | Power BI         | Interactive executive dashboard           |
| 05   | Documentation    | Project report + stakeholder presentation |
| 06   | GitHub           | Portfolio-ready repository                |

---

## Dataset Overview

| Attribute              | Value                                                    |
| ---------------------- | -------------------------------------------------------- |
| Source file            | `customer_shopping_behavior.csv`                         |
| Transactions           | **3,900**                                                |
| Original columns       | 18                                                       |
| Cleaned columns        | 19 (after feature engineering)                           |
| Total revenue          | **$233,081**                                             |
| Average purchase       | **$59.76**                                               |
| Average review rating  | **3.75 / 5.0**                                           |
| Missing values handled | 37 nulls in `Review Rating` (imputed by category median) |

**Key fields:** Age, Gender, Item Purchased, Category, Purchase Amount, Location, Season, Review Rating, Subscription Status, Shipping Type, Discount Applied, Previous Purchases, Payment Method, Frequency of Purchases.

---

## Key Insights (from SQL analysis)

### Revenue & Demographics
- **Male** customers generate **$157,890** (68% of revenue); **Female** customers have a slightly higher average ticket ($60.25 vs $59.54).
- **Young Adults** lead both revenue ($62,143) and average spend.

### Customer Segments (by previous purchases)
| Segment   | Definition              | Count     |
| --------- | ----------------------- | --------- |
| New       | 1 previous purchase     | 83        |
| Returning | 2–10 previous purchases | 701       |
| Loyal     | >10 previous purchases  | **3,116** |

The base is heavily skewed toward Loyal shoppers → high leverage for retention programs.

### Subscription
- Subscription rate: **27%** (1,053 customers).
- Average spend is nearly identical for subscribers vs non-subscribers → opportunity to add exclusive member value.

### Discounts
- 43% of orders used a discount.
- **839** discount users still spent *above* the overall average (avg $79.79).
- Most promo-dependent products: **Hat (50%)**, Sneakers (50%), Coat (49%), Sweater (48%), Pants (47%).

### Products
- Top-rated: Gloves (3.86), Sandals (3.84), Boots (3.82), Hat (3.80), Skirt (3.79).
- Category revenue mix: Clothing 45% · Accessories 32% · Footwear 15% · Outerwear 8%.

### Shipping
- Express shipping customers spend ~$2 more on average than Standard ($60.48 vs $58.46).

---

## Business Recommendations

1. **Boost subscription value** — Introduce exclusive benefits (early access, free Express shipping, member-only SKUs) so membership clearly increases LTV.
2. **Loyalty program for Returning segment** — Convert the 701 Returning customers into Loyal advocates with points/tiers.
3. **Discount discipline** — Protect margins on the 5 most promo-heavy SKUs with controlled price tests.
4. **Product positioning** — Feature top-rated and best-selling items in acquisition and retention campaigns.
5. **Targeted marketing** — Prioritize Young Adults and Express-shipping shoppers in paid and CRM channels.
6. **Gender-aware growth** — Balance assortment depth and messaging for both the high-volume male segment and higher-ticket female segment.

---

## Repository Structure

```text
customer-shopping-behavior-analysis/
│
├── data/
│   ├── raw/
│   │   └── customer_shopping_behavior.csv
│   └── processed/
│       └── customer_shopping_behavior_cleaned.csv
│
├── notebooks/
│   └── Sales_Project.ipynb          # Cleaning, EDA, feature engineering, DB load
│
├── sql/
│   └── customer_shopping_behavior.sql   # 10 business questions
│
├── dashboard/
│   └── customer_shopping_behaviour.pbix # Power BI interactive dashboard
│
├── reports/
│   ├── Customer_Shopping_Behavior_Project_Report.docx
│   └── Customer_Shopping_Behavior_Business_Presentation.pptx
│
├── images/                          # Screenshots / dashboard previews (optional)
│
├── Business Problem  Document.pdf  #Problem

└── README.md
```

---

## How to Reproduce

### 1. Python environment
```bash
pip install pandas sqlalchemy pymysql openpyxl
```

### 2. Run the notebook
Open `notebooks/Sales_Project.ipynb` and execute all cells:
- Loads raw CSV
- Imputes missing review ratings by category median
- Standardizes column names to snake_case
- Drops redundant `promo_code_used`
- Creates `age_group` and `purchase_frequency_days`
- Exports cleaned CSV
- (Optional) Loads data into MySQL/PostgreSQL

### 3. SQL analysis
Connect to your database and run the queries in `sql/customer_shopping_behavior.sql`.

### 4. Power BI
Open `dashboard/customer_shopping_behaviour.pbix` with Power BI Desktop (or publish to Power BI Service).

---

## Tools & Skills Demonstrated

| Area                  | Skills                                                                             |
| --------------------- | ---------------------------------------------------------------------------------- |
| **Data wrangling**    | pandas, missing-value imputation, feature engineering, column standardization      |
| **SQL**               | Aggregations, CTEs, window functions (`ROW_NUMBER`), CASE segmentation, subqueries |
| **Visualization**     | Power BI interactive dashboards                                                    |
| **Business analysis** | Problem framing, KPI definition, actionable recommendations                        |
| **Documentation**     | Professional report + stakeholder presentation                                     |
| **Version control**   | Clean, portfolio-ready GitHub structure                                            |

---

## Author
Jatoth Adithya Naik

[![GitHub](https://img.shields.io/badge/GitHub-adithya--naik-181717?style=for-the-badge\&logo=github\&logoColor=white)](https://github.com/adithya-naik)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Adithya%20Naik-0A66C2?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/adithyanaik/)


Built as a portfolio project demonstrating a complete, company-level data analytics workflow.

