# E-commerce Customer Behavior Analysis

> **Python Data Analytics Portfolio Project** · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook

## Overview

This project explores customer behavior, sales trends, category profitability, customer value segments, and potential cross-selling opportunities using Python. It turns transaction-level data into business questions, measurable findings, and recommendations.

**Dataset note:** The dataset is synthetic and intended for portfolio practice. These findings should not be represented as results from a real company.

## Business Questions

- How do net sales, estimated profit, and profit margin vary by product category?
- Which products and channels contributed most to the January-to-February Electronics sales change?
- How do customer segments differ in net sales and average order value (AOV)?
- How did monthly order volume and High Value customer Fashion revenue vary over time?
- What happened to customers who purchased Fashion in 2024 but not in 2025?
- How can a Fashion cross-sell campaign be evaluated with profit as the primary objective?

## Tools and Skills

- **Python:** analysis and reproducible workflow
- **Pandas / NumPy:** cleaning, grouping, joins, feature engineering, KPI calculations
- **Matplotlib / Seaborn:** charts and exploratory data analysis
- **Jupyter Notebook / Google Colab:** analysis and documentation
- **Business analytics:** segmentation, trend investigation, hypothesis development, experiment design

## Workflow

1. Load and validate the dataset.
2. Review missing values, duplicates, data types, and calculated fields.
3. Calculate net sales, estimated profit, margin, orders, and AOV.
4. Compare category sales and profitability.
5. Investigate month-to-month sales changes by product and channel.
6. Analyze customer segments and monthly order trends.
7. Explore High Value Fashion performance and customer category migration.
8. Design a proposed profit-focused cross-selling A/B test.
9. Document assumptions and limitations.

## Key Findings

The findings below are from the current analysis of the synthetic dataset.

- **Customer segments:** Returning customers have higher total net sales than new customers in the plotted comparison, while the new-customer group has a slightly higher AOV. The chart labels use `customer_type`, which is synthetic; treat this as exploratory only, not a reliable lifecycle analysis.
- **Category sales:** Electronics has the highest total net sales in the category chart.
- **Category profit:** Fashion contributes the highest estimated total profit in the plotted category comparison. Beauty has the highest profit margin, while Electronics has the lowest margin among the categories shown.
- **January-to-February Electronics change:** The product-level chart shows a large decline for Smartwatch and Jacket, while Monitor and Wireless Earbuds show the largest increases. These are changes in sales, not explanations of why sales changed.
- **Channel-level Smartwatch change:** The plotted channels all show a decline or near-zero decline from January to February; Paid Ads has the largest negative change in the chart.
- **Monthly trends:** Order volume varies substantially month to month. High Value customer Fashion revenue also fluctuates; the series does not show a steady, uninterrupted decline.

### Visual Findings
<img width="3000" height="1800" alt="Total Net Sales by Product Category" src="https://github.com/user-attachments/assets/94951b89-15db-4574-8c92-948e70f24ada" />


#### Customer segment sales and AOV
<img width="4500" height="1500" alt="Combined charts for customer analysis" src="https://github.com/user-attachments/assets/c8abe37b-44db-45c5-96df-bf141df0d254" />



#### Total net sales by category
<img width="3000" height="1800" alt="Total Net Sales by Product Category" src="https://github.com/user-attachments/assets/5cf06045-9d34-4ad9-91b4-39fed941274a" />



#### Estimated profit by category

<img width="3000" height="1800" alt="Estimated Profit by Product Category" src="https://github.com/user-attachments/assets/7ac65dae-14c5-4ccb-9ddb-e1a467543bb8" />



#### Profit margin by category

<img width="3000" height="1800" alt="Profit Margin by Product Category" src="https://github.com/user-attachments/assets/bb320299-dd1f-49a1-85bc-08475d70bd8e" />


#### Electronics product sales change, January to February
<img width="3000" height="1800" alt="Electronics Product Sales Change From Jan to Feb" src="https://github.com/user-attachments/assets/17c04033-d1e3-4e73-bb40-fb53f7438127" />


#### Smartwatch sales change by channel
<img width="3000" height="1500" alt="Smartwatch Sales Change by Channel" src="https://github.com/user-attachments/assets/2e7dfe52-3b36-4440-9e9e-f984ae5e7dc8" />



#### Monthly order volume
<img width="4200" height="1500" alt="Monthly Orders Trend" src="https://github.com/user-attachments/assets/bc7a67cd-4ae4-4cc6-b3f8-57f58625dbf3" />




#### Monthly Fashion revenue for High Value customers

<img width="3600" height="1500" alt="Monthly Fashion Revenue — High Value Customers" src="https://github.com/user-attachments/assets/ac0873fd-3c90-402d-b352-8966f0d70b07" />



## Proposed Cross-Selling Experiment

The project proposes a Fashion cross-sell experiment for eligible former Fashion customers who purchased Beauty. The primary metric is net profit per randomized customer, with purchase rate, Fashion revenue, and customer experience as supporting/guardrail measures.

**This experiment has not been run prospectively.** The historical treatment/control comparison and bootstrap interval are exploratory and cannot establish a causal campaign effect. A real experiment requires random assignment before outreach, a fixed outcome window, a pre-specified minimum detectable effect, and an adequate sample size.

## Repository Structure

```text
ecommerce-customer-behavior-analysis/
├── README.md
├── Ecommerce_Sales_Profitability_Analysis.ipynb
├── ecommerce_portfolio_dataset_15000.csv
├── images/
│   ├── customer-segment-sales-aov.png
│   ├── total-net-sales-by-category.png
│   ├── estimated-profit-by-category.png
│   ├── profit-margin-by-category.png
│   ├── electronics-product-sales-change-jan-feb.png
│   ├── smartwatch-sales-change-by-channel.png
│   ├── monthly-orders-trend.png
│   └── monthly-fashion-revenue-high-value-customers.png
└── docs/
    ├── REVIEW_NOTES.md
    └── resume_and_interview.md
```

## How to Run

### Google Colab
1. Upload the notebook to Google Colab.
2. Upload `ecommerce_portfolio_dataset_15000.csv` into the session.
3. Ensure the notebook reads the uploaded CSV path.
4. Choose **Runtime → Run all** and check the outputs.

### Local environment
Install dependencies:

```bash
python -m pip install pandas numpy matplotlib seaborn jupyter
```

Then run:

```bash
jupyter notebook
```

Open the notebook and run all cells from a fresh kernel.

## Limitations

- The dataset is synthetic and does not represent real business performance.
- Describe `profit_inr` as **estimated profit** unless its cost coverage is verified.
- The synthetic `customer_type` field is not a dependable lifecycle classification.
- Customer segments created from full-period revenue are retrospective and can introduce look-ahead bias in historical comparisons.
- Historical group comparisons do not prove a campaign caused a change.
- A sample-size estimate based on a small historical sample is uncertain and should be recalculated using comparable customer-level outcomes.

## Potential Next Steps

- Build a Power BI dashboard using the same validated KPI definitions.
- Add SQL versions of core KPI and customer-segmentation queries.
- Validate the notebook from a fresh runtime before publication.
- If business data becomes available, test cross-selling prospectively with randomized assignment.

## Author

**Vinit Nimbalkar** · Data Analytics Portfolio Project
