# Retail Sales ETL Pipeline — Alteryx Designer

![Alteryx](https://img.shields.io/badge/Tool-Alteryx%20Designer-1A6B3C?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-1D9E75?style=flat)
![Dataset](https://img.shields.io/badge/Dataset-1%2C000%20Orders-2E75B6?style=flat)
![Type](https://img.shields.io/badge/Type-ETL%20%7C%20Data%20Wrangling-BA7517?style=flat)

An end-to-end ETL and data wrangling workflow built in Alteryx Designer on a dataset of 1,000 Indian retail orders. The workflow automates data cleansing, transformation, aggregation, and ranked summary output — replacing a manual Excel pivot process.

---

## ETL Workflow — 9 Steps

| Step | Tool | What it does |
|------|------|-------------|
| 1 | Input Data | Loads retail_sales.csv — 1,000 rows, 14 columns |
| 2 | Data Cleansing | Removes leading/trailing whitespace; replaces nulls with 0 |
| 3 | Select | Retains 8 key columns: Order ID, Region, Category, Sub-Category, Sales Amount, Profit, Discount (%), Delivery Status |
| 4 | Filter | Removes 333 returned orders — [Delivery Status] != "Returned" |
| 5 | Formula | Derives new column: Profit Margin % = [Profit] / [Sales Amount] * 100 |
| 6 | Summarise | Groups by Region + Category → Sum of Sales, Sum of Profit, Count of Orders, Avg Margin % |
| 7 | Formula | Recalculates Overall Margin % at group level |
| 8 | Sort | Orders by Total Sales descending — ranks top-performing segments |
| 9 | Output Data | Exports region_category_summary.csv — final clean deliverable |

---

## Tools Used

`Input Data` `Output Data` `Data Cleansing` `Select` `Filter` `Formula` `Summarise` `Sort`

---

## Key Findings from Output

- **East region** leads with highest total sales across all categories
- **Furniture** is the top revenue category at 36.6% of total sales
- **Profit margins** range from 11.87% (South) to 12.81% (East)
- **333 returned orders** (33.3%) were excluded — flagged as a business risk
- **Stapler** has the highest profit margin among all sub-categories

---

## Input Dataset

| Field | Detail |
|-------|--------|
| Name | Indian Retail Sales Dataset |
| Source | Kaggle |
| Rows | 1,000 orders |
| Columns | 14 — Order ID, Date, Customer, Region, City, Category, Sub-Category, Product, Sales, Quantity, Discount, Profit, Delivery Status, Payment Method |

---

## Output File

**region_category_summary.csv** — aggregated summary table with:
- Region and Category grouping
- Total Sales (₹)
- Total Profit (₹)
- Overall Profit Margin %
- Order Count

---

## Skills Demonstrated

`Alteryx Designer` `ETL Pipeline` `Data Wrangling` `Data Cleansing`
`Workflow Automation` `Data Transformation` `Aggregation` `Data Analytics`

---

*Built as part of Data Analyst job preparation — Hyderabad, 2025*
