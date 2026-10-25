# Data and Methodology Notes

## Dataset
The project uses `ecommerce_portfolio_dataset_15000.csv`, a synthetic dataset with 15,000 rows and 23 columns. Its observed date range is 2024-01-01 through 2025-12-31.

## Metric definitions
- **Net sales:** sum of `net_sales_inr`.
- **Estimated profit:** sum of `profit_inr`; verify whether all variable and campaign costs are included before calling it contribution profit.
- **Profit margin:** estimated profit / net sales × 100.
- **Average order value (AOV):** net sales / distinct order IDs.
- **Customer segment:** tertile of customer-level total net sales over the full dataset.

## Data-quality notes
The dataset has missing values in fields including customer rating, shipping days, sales channel, discount percentage, payment method, and city. Preserve the difference between missing values and true zeros. Use category-level imputation only when justified and document it.

## Experiment notes
The proposed experiment targets customers who bought Fashion in 2024, did not buy Fashion in 2025, and bought Beauty in 2025. It is a small historical cohort and is not sufficient by itself to establish campaign impact. A valid A/B test must assign customers before the measurement period, keep assignment stable, measure both groups over the same window, account for campaign costs, and report uncertainty.

## Important corrections from the uploaded notebook
- A KPI labelled “Total Net Sales” was calculated from `gross_sales_inr`; the cleaned notebook uses `net_sales_inr`.
- The uploaded notebook contained repeated exploratory cells and multiple definitions of the Fashion retention population. The cleaned notebook states its segment scope explicitly.
- The uploaded notebook's historical December comparison was not a causal A/B test because assignments were generated after the historical measurement window.
