# 📦 Item Sales Performance Analysis

🌐 **English** | [العربية](README.ar.md) · [← Back to portfolio](../README.md)

A one-page Power BI report on item-level sales: revenue, cost of goods, profit and margin, with monthly seasonality, a state breakdown, and the best-selling items.

![Report](assets/report.png)

## Business questions

- How much does the business sell, what does it cost, and how profitable is it?
- Which items and states drive sales?
- Is there a seasonal pattern across months?
- How concentrated is revenue in a few items?

## Dataset

A star schema built from the Wide World Importers sample (a novelty and packaging wholesaler).

| File | Role | Rows |
|------|------|------|
| `FactSale.csv` | Fact table: one row = one sale line | 26,397 |
| `DimCity.csv` | City, state, country, territory | 13,028 |
| `DimCustomer.csv` | Customers | 403 |
| `DimDate.csv` | Calendar | 1,460 |
| `DimStockItem.csv` | Items | 673 |
| `DimEmployee.xlsx` | Salespeople | 212 |

Sales period: **2013-01-01 to 2016-05-31**. Cleaning and relationships were done in Power Query and the model view.

## Dashboard content

- KPIs: total sales excl. tax, COGS, total profit, profitability %.
- Line chart: total sales by month.
- Table: sales, quantity, and sales-line count by state.
- Bar chart: total sales and quantity by stock item.

## Key findings (verified against the data)

| KPI | Value |
|-----|-------|
| Total sales (excl. tax) | $19.88M |
| COGS | $9.96M |
| Profit | $9.92M |
| Profitability | 49.9% |
| Quantity | 1,028,670 units |

| State | Sales |
|-------|-------|
| California | $8.83M |
| Washington | $4.23M |
| Alaska | $3.00M |
| Oregon | $2.25M |
| Nevada | $1.25M |
| Hawaii | $0.32M |

- California alone is **44%** of sales, and the top two states are 66%.
- The best item is **Air cushion machine (Blue)** at about **$1.2M**.
- The top 10 items (of 227 sold) generate **33%** of revenue, the top 20 generate **44%**.
- Monthly sales run from about $1.2M (August) to $2.1M (May). Note that the data holds four Januaries to Mays but only three Junes to Decembers (2016 stops in May), so spring months look stronger than they are.

> Correction: the old table labeled a column "Salesperson Count" with 26,397 in total. That number is the count of sales lines, not salespeople (the data has 99 distinct salespeople). It is relabeled here.

## Recommendations

- Prioritize inventory and promotion for the top items, and review the long tail.
- Study what works in California and Washington and replicate it in smaller states.
- Compare months on a like-for-like basis (same years) before planning around seasonality.
- Watch margin by item: the average is about 50%, so low-margin items deserve a review.

## Tools

Power BI Desktop · DAX (sales, COGS, profit, margin) · Power Query · star schema modeling

## Files

```
Item-Sales-Performance-Analysis/
├── Item-Sales-Dashboard.pbix
├── data/                # fact and dimension tables
└── assets/report.png
```

## How to open

Open `Item-Sales-Dashboard.pbix` in Power BI Desktop. Point the data source to the `data/` folder if asked.
