# Retail Intelligence & Customer Profitability Analytics

End-to-end retail analytics project using **Python, Pandas, DuckDB, SQL, and Power BI**.

## Project Overview

This project analyzes a relational e-commerce dataset across customers, orders, order items, products, categories, payments, and returns. The workflow moves from data profiling and quality validation through analytical modeling and executive dashboard reporting.

### Business Questions

- Which categories generate the most profit?
- Which products generate high revenue but relatively lower margins?
- How does customer loyalty relate to customer value?
- Which countries generate the most revenue and profit?
- What is the impact of returns and refunds?
- How concentrated is revenue among high-value customers?
- What seasonal patterns appear in revenue?

## Analytical Workflow

**Raw relational data → Python/Pandas data audit → DuckDB analytical layer → SQL metric views → Power BI**

### Data Audit

The analysis includes:
- table profiling
- null analysis
- duplicate checks
- relationship validation
- financial validation
- payment fan-out investigation
- record-level spot checks

A payment fan-out check was performed before constructing the sales fact model so that multiple payment records would not incorrectly multiply sales values.

## Key Results

| Metric | Result |
|---|---:|
| Revenue | $9.02M |
| Profit | $3.58M |
| Profit Margin | 39.68% |
| Returns | 12,000 |
| Refund Amount | $498K |
| Refund Rate | 5.52% |
| Top 1% Revenue Share | 56.43% |
| Top 10% Revenue Share | 79.08% |
| Champion Revenue | $7.75M |
| Champion Revenue Share | 85.87% |

## Customer Intelligence

RFM analysis was used to segment customers into:
- Champions
- Loyal Customers
- Potential Loyalists
- At Risk
- Others

The analysis found substantial revenue concentration among high-value customer groups. These results describe observed customer patterns; they do not establish causation.

## Product & Category Insights

The analysis identified:
- Fertiliser as the highest-profit category.
- Bulbs and Hoses as major profit contributors.
- Several high-revenue products with comparatively lower margins, including Heritage Steel Watering Can, Heritage Steel Hand Fork, and Heritage Steel Secateurs.

## Geographic & Seasonal Analysis

The project compares revenue and profit across countries and channels and investigates monthly revenue patterns. GB, US, and CA were among the leading markets, while November and December showed notable revenue increases in the analyzed period.

## Power BI Dashboard

The report contains three focused pages:

1. **Executive Overview** — revenue, profit, margin, orders, customers, country and channel performance, and monthly trends.
2. **Customer Analytics** — customer concentration, RFM segments, and loyalty-tier analysis.
3. **Product Analytics** — category profitability, product revenue, and high-revenue/lower-margin products.

## Technology Stack

- Python
- Pandas
- NumPy
- DuckDB
- SQL
- Power BI
- Power Query
- DAX
- Jupyter Notebook

## Repository Structure

```text
retail-intelligence-customer-profitability/
├── README.md
├── .gitignore
├── notebooks/
│   └── retail_intelligence_analysis.ipynb
├── powerbi/
│   └── retail_intelligence.pbix
├── screenshots/
│   ├── executive-overview.png
│   ├── customer-analytics.png
│   └── product-analytics.png
├── data/
│   └── README.md
└── docs/
    └── methodology.md
```

## Data

The project uses the SQLShed Ecommerce Orders practice dataset.

Source: https://sqlshed.com/practice-datasets/ecommerce-orders/

Raw data files are intentionally excluded from this repository. Do not commit customer-level records or other sensitive source data.

## Limitations

- The analysis identifies patterns and associations, not causal relationships.
- RFM segments are based on the selected snapshot date and quantile-based scoring approach.
- Cohort analysis was not performed.
- Advanced SQL techniques such as CTEs or window functions should only be claimed if they are actually present in the notebook.
- Dashboard findings depend on the source dataset and its definitions.

## Author

**Mary Oluropo**  
Data Analyst | Business Intelligence | Power BI

Portfolio: https://nifemi-the-analyst-portfolio.netlify.app/  
LinkedIn: https://linkedin.com/in/mary-oluropo-336812263
