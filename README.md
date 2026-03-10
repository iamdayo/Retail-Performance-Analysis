# Where Is the Profit Going?
## Retail Orders - Business Performance Analysis
**Tool:** Microsoft Excel | **By:** Temidayo Olubayo

Revenue is growing, but hidden losses inside the product portfolio are quietly eroding profitability.

## Business Context
Retail businesses often focus heavily on revenue growth, but revenue alone does not determine if a business is financially healthy. Profit margins, product performance and customer segment dynamics play a critical role in long-term sustainability.

This analysis investigates sales performance across products, regions, and customer segments to uncover hidden profitability issues and identify opportunities for strategic improvement.

The goal is to understand **where revenue is coming from, where profit is leaking, and which parts of the business deserve more attention.**

## Table of Contents

1. [Project Overview](#project-overview)
2. [Dataset Overview](#dataset-overview)
3. [Data Cleaning](#data-cleaning)
4. [Data Merging](#data-merging)
5. [Workbook Structure](#workbook-structure)
6. [Dashboard](#dashboard)
7. [Key Findings](#key-findings)
8. [Recommendations](#recommendations)
9. [Tools Used](#tools-used)

## Project Overview

This project analyzes retail sales transactions to understand overall business performance, profitability patterns, and product portfolio health.

Using Microsoft Excel, three separate datasets were cleaned, merged, and transformed into a single analytical dataset. Pivot tables and charts were then used to build an interactive dashboard that highlights key performance indicators and business trends.

The analysis focuses on answering questions such as:

- Which products and categories drive the most revenue?
- Are high-revenue categories actually profitable?
- Which customer segments and regions contribute most to sales?
- Where are hidden losses occurring within the product portfolio?

## Dataset Overview

The raw data came in three separate sheets.

| Sheet | Rows | Columns | Description |
|---|---|---|---|
| Transactions | 9,749 | 6 | Order-level records including Order ID, Date, Ship Mode, Customer ID, Product ID, Quantity |
| Customers | 794 | 8 | Customer details including Name, Segment, Region, City, State, Postal Code |
| Products | 1,692 | 6 | Product catalog including Name, Category, Sub-Category, Price and Cost |

After cleaning and validation, **8,412 transaction records** remained for analysis.

## Data Cleaning

Before analysis, the datasets were cleaned to ensure consistency and reliability.

Key steps included:

- **Duplicate removal**  
  Rows were only removed when every column matched exactly, ensuring only single rows were preserved
  
- **Text standardization**  
  `PROPER()` was applied to names, cities, states, and product descriptions to correct inconsistent formatting.

- **Numeric formatting corrections**  
  Price and cost columns were standardized to two decimal places.

- **Postal code correction**  
  Postal codes were converted to text format to preserve leading zeros.

- **Date validation**  
  Order dates were standardized to a consistent `MM/DD/YYYY` format.

Post-cleaning dataset: **8,412 transactions**

## Data Merging

All three datasets were merged into a single **Cleaned Data** sheet.

The `Transactions` sheet served as the base table, while customer and product attributes were merged using `XLOOKUP`.

Final dataset structure:

**8,412 rows × 23 columns**

_Data was additionally validated and merged using Power Query as a secondary check to confirm the integrity of the XLOOKUP-merged dataset_

## Workbook Structure

The Excel workbook contains six sheets:

| Sheet | Purpose |
|---|---|
| Transactions | Raw transaction data |
| Customers | Raw customer dataset |
| Products | Raw product catalog |
| Cleaned Data | Final merged analytical dataset |
| Pivot Tables | All pivot table analysis |
| Dashboard | Interactive business performance dashboard |
| Insights | Insights derived from the analysis |

## Dashboard

The dashboard was designed to answer key business questions rather than simply display metrics.

### KPI Cards

- Total Sales — **$7.89M**
- Total Profit — **$1.09M**
- Profit Margin — **13.76%**
- Total Orders — **8,412**
- Best Performing Year — **2017 ($2.47M)**
- YoY Growth (2016 → 2017) — **8.92%**

### Charts

- Top 5 Products by Revenue
- Sales vs Profit by Category
- Sales by Region (Quantity)
- Monthly Sales Trend
- Sales Distribution by Ship Mode

### Interactive Filters

- Year
- Quarter
- Region
- Product Category

<img width="1495" height="853" alt="image" src="https://github.com/user-attachments/assets/cba2f6d7-cb54-40fc-a017-5a1ca41615fb" />

## Key Findings

### Revenue growth in 2016 was driven by a single category:

Technology sales more than doubled in 2016, creating a **39% revenue spike**. However, the growth was concentrated in one category rather than distributed across the business.

This suggests the business experienced **category-driven growth rather than company-wide expansion.**
<img width="1101" height="237" alt="image" src="https://github.com/user-attachments/assets/0bb1407d-6926-4d96-8888-1491ce9480d3" />


### Overall margins leave little room for error:

The company generated **$7.89M in revenue**, but only **$1.09M in profit**, resulting in a **13.76% margin**.

At this margin level, small shifts in supplier costs or pricing strategy could significantly impact profitability.

### Hundreds of products are operating at a loss:

The analysis revealed **449 products generating negative profit**.

These losses are masked by profitable products within the overall portfolio, making them difficult to detect without deeper analysis.
<img width="1162" height="730" alt="image" src="https://github.com/user-attachments/assets/60f9a9fc-92f4-4a8c-a0b8-f481663f0b9e" />


### Furniture category underperforms:

Furniture shows the **highest sales volume** among categories but produces the **lowest profit margin (12.5%)**.

High activity without strong profitability suggests structural cost issues within the category.
<img width="1205" height="301" alt="image" src="https://github.com/user-attachments/assets/2add5bbe-2ce6-4583-a122-b3d680b1e56f" />


### Corporate customers generate weaker margins:

The Corporate segment's profit margin trails the Consumer segment by about **2%**.

It is having a lot of orders but low profit margin, and may be as a result of overdiscounting in the corperate segment.
<img width="1097" height="216" alt="image" src="https://github.com/user-attachments/assets/057b0e13-03db-4976-8bd3-7ac3c973a814" />

## Recommendations

**1. Address the 449 loss-making products:**

These products require clear decisions: discontinue, reprice, or renegotiate supplier costs.

**2. Build growth beyond Technology:**

Technology drove the strongest revenue year, but relying on a single category increases risk.

**3. Investigate Furniture cost structure:**

Improving supplier terms or pricing strategy could significantly improve profitability.

**4. Review Corporate pricing strategy:**

Corporate deals appear to involve aggressive discounting that reduces margins.

**5. Protect margins:**

At a **13.76% margin**, profitability protection should become a strategic priority.

## Tools Used

| Tool | Purpose |
|---|---|
| Microsoft Excel | Data cleaning, merging, analysis |
| Excel Formulas | Calculations and feature engineering |
| Power Query | Data cleaning and merge validation |
| Pivot Tables | Aggregation and business analysis |
| Charts & Slicers | Dashboard and interactive exploration |

### Temidayo Olubayo  |  Data Analytics  

**Temidayo Olubayo**  
Data Analytics | Excel | SQL | Power BI

Additional calculated fields were then created:
