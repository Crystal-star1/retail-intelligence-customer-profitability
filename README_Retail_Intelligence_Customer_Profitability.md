# Retail Intelligence & Customer Profitability Analytics

An end-to-end retail analytics project focused on revenue, profitability, customer concentration, product performance, returns, and business intelligence reporting.

The project combines **Python, Pandas, DuckDB, SQL, RFM segmentation, and Power BI** to transform a multi-table e-commerce dataset into decision-ready analysis and executive dashboards.

## Project Overview

This project builds an analytical workflow from relational e-commerce data through data validation, analytical modeling, SQL analysis, customer segmentation, and Power BI reporting.

The analysis focuses on understanding:
- Where revenue comes from
- Which categories and products generate profit
- How concentrated customer value is
- Which customer segments are most valuable
- Where returns and refunds affect performance
- Which markets and channels contribute most to the business

## Business Questions

1. Which product categories generate the most profit?
2. Which products generate high revenue but comparatively lower margins?
3. How does customer loyalty relate to customer value?
4. Which countries generate the most revenue and profit?
5. What is the impact of returns and refunds on revenue?
6. How concentrated is revenue among the customer base?
7. How does revenue and profitability change over time?
8. Which customer segments should receive different levels of attention?

## Data

The project uses a relational e-commerce dataset containing seven connected tables:

- Customers
- Orders
- Order Items
- Products
- Categories
- Payments
- Returns

### Data Quality Checks

The workflow included:
- Null-value analysis
- Duplicate checks
- Relationship validation
- Date-range validation
- Financial validation
- Record-level spot checks
- Payment fan-out investigation
- Sales calculation validation

A key data-quality issue investigated was the relationship between orders and payments. Directly joining payment records into the sales fact table can multiply transaction rows when multiple payments exist for an order. The analysis therefore treated payments carefully to avoid overstating revenue and profit.

## Analytical Workflow

```text
Relational E-Commerce Data
          ↓
Python + Pandas
          ↓
Data Profiling & Validation
          ↓
DuckDB Analytical Storage
          ↓
SQL Metric Modeling
          ↓
Customer & Product Analysis
          ↓
RFM Customer Segmentation
          ↓
Power BI
          ↓
Executive Insights & Reporting
```

## Key Results

| Metric | Result |
|---|---:|
| Revenue | **$9.02M** |
| Profit | **$3.58M** |
| Profit Margin | **39.68%** |
| Returns | **12,000** |
| Refund Amount | **$498K** |
| Refund Rate | **5.52%** |
| Top 1% Customer Revenue Share | **56.43%** |
| Top 5% Customer Revenue Share | **72.35%** |
| Top 10% Customer Revenue Share | **79.08%** |
| Champion Segment Revenue | **$7.75M** |
| Champion Segment Revenue Share | **85.87%** |

## Customer Analysis

Customer value was analyzed using **RFM segmentation**:
- Recency
- Frequency
- Monetary value

The resulting customer segments included:
- Champions
- Loyal Customers
- Potential Loyalists
- At Risk
- Others

The top 1% of customers accounted for **56.43% of revenue**, while the top 10% accounted for **79.08%**.

## Product & Category Analysis

The analysis compared products and categories using:
- Revenue
- Cost
- Profit
- Profit margin
- Units sold

The highest-profit categories included:
- Fertiliser
- Bulbs
- Hoses
- Fire Pits
- Bagged Soil

The analysis also identified products generating substantial revenue while producing comparatively lower margins, including:
- Heritage Steel Watering Can
- Heritage Steel Hand Fork
- Heritage Steel Secateurs

## Geographic & Seasonal Analysis

The analysis examined revenue and profitability across countries and over time.

The strongest markets included:
- United Kingdom
- United States
- Canada

Revenue also showed noticeable seasonal increases during **November and December**.

# Power BI Dashboard

The final Power BI report contains three analytical pages.

### 1. Executive Overview
- Revenue
- Profit
- Profit margin
- Orders
- Customers
- Revenue trends
- Country performance
- Channel performance

### 2. Customer Analytics
- RFM segmentation
- Customer concentration
- Loyalty tiers
- Customer value distribution

### 3. Product Analytics
- Category profitability
- Product revenue
- Product performance
- High-revenue / lower-margin products

## Dashboard Screenshots

Add the three dashboard screenshots to the `screenshots/` folder using these filenames:
- `executive-overview.png`
- `customer-analytics.png`
- `product-analytics.png`

### Executive Overview

![Executive Overview](screenshots/executive-overview.png)

### Customer Analytics

![Customer Analytics](screenshots/customer-analytics.png)

### Product Analytics

![Product Analytics](screenshots/product-analytics.png)

## Technology Stack

### Python
- Python
- Pandas
- NumPy
- Data profiling
- Data validation
- RFM analysis

### SQL & Analytics
- DuckDB
- SQL
- Relational data modeling
- Analytical views
- Metric calculations

### Business Intelligence
- Microsoft Power BI
- Power Query
- DAX
- KPI reporting
- Interactive dashboards

## Repository Structure

```text
retail-intelligence-customer-profitability/
│
├── data/
│   └── README.md
├── docs/
│   └── methodology.md
├── notebooks/
│   └── retail_intelligence_analysis.ipynb
├── powerbi/
│   └── Retail_Intelligence_Project.pbix
├── screenshots/
│   ├── executive-overview.png
│   ├── customer-analytics.png
│   └── product-analytics.png
├── .gitignore
└── README.md
```

## Reproducibility

The public repository does **not** contain the raw customer-level source data.

To reproduce the analysis:
1. Obtain the source dataset from the original provider.
2. Place the required Parquet files in the appropriate data directory.
3. Open the analysis notebook.
4. Run the data profiling and validation workflow.
5. Build the DuckDB analytical layer.
6. Run the SQL analysis.
7. Use the resulting analytical data for Power BI reporting.

The public analytical workflow excludes customer personally identifiable information from the final analytical model.

## Data Source

The project uses the **SQLShed Ecommerce Orders** practice dataset.

Source: https://sqlshed.com/practice-datasets/ecommerce-orders/

The dataset contains interconnected e-commerce tables covering customers, orders, order items, products, categories, payments, and returns.

## Important Limitations

This project is an analytical case study rather than a production retail system.

The analysis identifies patterns and relationships in the available data. It does **not** establish causal relationships between variables.

RFM segmentation is used for customer analysis. Cohort analysis is not part of this project.

Results should therefore be interpreted within the scope of the dataset, its definitions, and the analytical assumptions documented in the repository.

## Related Work

**Portfolio:**  
https://nifemi-the-analys.netlify.app/

**LinkedIn:**  
https://linkedin.com/in/mary-oluropo-336812263

**Medium:**  
_Add the Medium article link after the article is finalized._

## Author

**Mary Oluropo**

Data Analyst | Business Intelligence | Power BI

Building practical analytics projects with Python, SQL, Power BI, and business intelligence.

## License

This repository contains original analysis, documentation, and project work created by the author.

The underlying dataset is subject to the terms of its original source.
