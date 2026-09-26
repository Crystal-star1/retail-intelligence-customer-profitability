# Methodology

## 1. Data Profiling
Profile the source tables for dimensions, columns, data types, missing values, duplicates, categorical distributions, and date ranges.

## 2. Data Quality
Validate nulls, duplicates, relationships, financial values, record-level samples, and payment fan-out risk.

## 3. Analytical Model
Construct the sales fact model at order-item grain and enrich it with order, customer, product, and category information.

Payments were investigated separately before the fact model to avoid multiplying sales values when an order has multiple payment records.

## 4. DuckDB and SQL
Use DuckDB as the analytical query layer and create reusable views for fact sales, customer metrics, product metrics, category metrics, and channel metrics.

## 5. Customer Analysis
Use RFM scoring to create descriptive customer segments such as Champions, Loyal Customers, Potential Loyalists, At Risk, and Others.

## 6. Business Analysis
Evaluate profitability, customer value, geographic performance, channel performance, returns/refunds, and seasonality.

## 7. Dashboard
Present the analysis through focused Executive, Customer, and Product Power BI pages.
