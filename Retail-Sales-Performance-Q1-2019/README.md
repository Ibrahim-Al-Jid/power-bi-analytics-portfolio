# 🛒 Retail Sales Performance, Q1 2019

🌐 **English** | [العربية](README.ar.md) · [← Back to portfolio](../README.md)

A one-page Power BI dashboard on the first quarter of 2019 for a three-branch supermarket chain: sales, cost, gross income, and how they split by city, branch, product line, and customer gender.

![Dashboard](assets/dashboard.png)

## Business questions

- How much did the business sell in Q1 and how much was profit?
- Which cities, branches, and product lines perform best?
- How does buying behavior differ by gender?
- How do months and days of the month compare?

## Dataset

| Item | Value |
|------|-------|
| File | `data/supermarket_sales - Sheet1.csv` |
| Grain | One row = one invoice |
| Rows | 1,000 invoices, 19 columns |
| Period | 2019-01-01 to 2019-03-30 |
| Cities and branches | Yangon (A), Mandalay (B), Naypyitaw (C) |
| Product lines | 6 |

**Data quality.** Invoice `665-32-9167` has the invalid date `eeeeee`. The dashboard total (322.89K) equals the CSV total (322.97K) minus this invoice (76.15), so the row appears to be dropped by the report. The source file is left unchanged so the issue stays visible.

## Dashboard content

- Filters: month and day.
- KPIs: Sum of Total 322.89K, Sum of cogs 307.51K, Sum of gross income 15.38K.
- Monthly trend of total sales vs gross income.
- Donut and pie charts: sales by city and by branch.
- Bar charts: gross income and quantity by product line.
- Sales by gender and a product line treemap.

## Key findings (from the CSV)

| City / Branch | Total sales |
|---------------|-------------|
| Naypyitaw / C | 110.57K (34.2%) |
| Yangon / A | 106.20K (32.9%) |
| Mandalay / B | 106.20K (32.9%) |

- **Naypyitaw (Branch C) leads** by about 4K; the other two are practically tied.
- **Food and beverages** has the highest sales (56.14K) and gross income (2.67K). Health and beauty is lowest (49.12K).
- Electronic accessories sell the most units (971).
- Female customers account for 167.9K and male customers for 155.1K, about 52% vs 48%.
- Gross income is only about **4.8% of total sales** (15.38K of 322.89K). The margin is thin and is fixed at 4.76% on every invoice, because `gross income` is the 5% tax column.

> Heads-up: the `gross margin percentage` and `gross income` columns in this public dataset are derived from the 5% tax, so profitability here should be read as a demonstration, not as true retail margin. The dashboard "Sum of cogs" KPI (307.51K) also differs slightly from the CSV `cogs` column sum (307.07K after excluding the bad row); it equals the total minus gross income.

## Recommendations

- Fix the date entry problem at source so no invoice is dropped.
- Investigate why Branch C sells more and copy its practices to A and B.
- Focus on food and beverages and electronic accessories for promotions.
- Use the day and month slicers to catch short-term dips (February is the weakest month).

## Tools

Power BI Desktop · DAX · Power Query · donut, treemap, and combo visuals

## Files

```
Retail-Sales-Performance-Q1-2019/
├── Sales Report For 1Qrt 2019.pbix
├── data/supermarket_sales - Sheet1.csv
└── assets/dashboard.png
```

## How to open

Open `Sales Report For 1Qrt 2019.pbix` in Power BI Desktop and point the source to the CSV in `data/` if asked.
