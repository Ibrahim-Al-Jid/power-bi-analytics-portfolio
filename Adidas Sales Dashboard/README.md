# 👟 Adidas Sales Dashboard

🌐 **English** | [العربية](README.ar.md) · [← Back to portfolio](../README.md)

A one-page executive Power BI dashboard on sales from 2016 to 2018: headline financial KPIs, net sales by category and city, and monthly seasonality.

![Dashboard](assets/dashboard.png)

## Business questions

- How large is net revenue, and how much do discounts take away?
- Which product categories drive revenue?
- Which cities sell the most?
- Is there seasonality across months and years?

## Dashboard content

| Element | What it shows |
|---------|---------------|
| Filters | Year range slider (2016 to 2018) and category selector |
| KPIs | Gross sales $217.6M, discount value $27.2M, net sales $190.4M, quantity 6M units |
| Map | Net sales by Egyptian city: Alexandria, Cairo, Giza, Port Said, Ismailia, Luxor, Sharm El Sheikh |
| Bar chart | Net sales by category: Bikes $148.14M, Clothing $22.65M, Accessories $12.13M, Components $7.49M |
| Sankey | Net sales flow by year and city |
| Area chart | Net sales by month |

## Key findings

- **Bikes bring about 78% of net sales** ($148.14M of $190.4M). The other three categories together are about 22%.
- Discounts cut gross sales by about **12.5%** ($27.2M of $217.6M).
- Monthly net sales stay in a narrow band of roughly $15M to $16.2M. February is the lowest month ($14.84M); January, March, May, October and December are the highest.
- Sales are spread across seven Egyptian cities; use the map and Sankey to compare them by year.

## Recommendations

- Protect and grow the Bikes category, since it carries the revenue.
- Review the discount policy against margin: 12.5% is a large share of gross sales.
- Plan promotions around the flat seasonal curve rather than waiting for one peak.
- Test the weaker categories (Components, Accessories) with city-specific campaigns.

## About the data

This is a practice dashboard styled with Adidas branding. The categories (Bikes, Clothing, Accessories, Components) and Egyptian cities show that the underlying dataset is a sample or synthetic one, not real Adidas company data. The data model is embedded inside the `.pbix` file; no raw data file is included in this folder. Treat the numbers as a demonstration of dashboard design and DAX, not as real company results.

## Tools

Power BI Desktop · DAX (KPI measures) · Power Query · map visual · Sankey custom visual

## Files

```
Adidas Sales Dashboard/
├── Addidas Sales_new.pbix     # dashboard (file name keeps its original spelling)
└── assets/dashboard.png
```

## How to open

Open `Addidas Sales_new.pbix` in Power BI Desktop. The Sankey chart needs a custom visual, which Power BI will offer to load.
