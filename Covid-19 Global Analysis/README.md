# 🌍 COVID-19 Global Analysis

🌐 **English** | [العربية](README.ar.md) · [← Back to portfolio](../README.md)

A four-page Power BI report on the first nine months of the pandemic: how cases and deaths evolved, how countries and continents compare, and whether stricter government response went with better outcomes.

![Overview](assets/overview.png)

## Business questions

- How did cases and deaths develop over time, globally and by continent?
- Which countries were hit hardest once population size is taken into account?
- Is a higher government stringency index linked to fewer new cases?
- Where is the fatality rate high even though case counts are moderate?

## Dataset

| Item | Value |
|------|-------|
| Source | Our World in Data COVID-19 dataset (`owid-covid-data.csv`, raw) |
| Cleaned file | `dataset before & after/cleaned_covid_data.csv` |
| Period | 2019-12-31 to 2020-09-19 (daily) |
| Grain | One row = one country on one day |
| Countries | 210 (clean) |
| Rows | 44,785 raw, 44,257 clean |

**What cleaning changed.**
- Removed the aggregate rows `World` and `International` (528 rows) so that totals are not double counted.
- Added four columns: `cfr` (case fatality rate), `active_cases`, `total_cases_prev`, `growth_rate`, used for the trend indicator.

## Report pages

### 1️⃣ Overview
Global KPIs (cumulative cases and deaths, case fatality rate, average new cases per million), new cases vs new deaths over time, average new cases per million by continent, a world map, and filters for date, continent, and location.

### 2️⃣ Country deep dive
![Country deep dive](assets/country_deep_dive.png)

Pick a country to see its KPIs, trend, average stringency index, and a comparison against its continent and the global average.

### 3️⃣ Relationships
![Relationships](assets/relationships.png)

Two bubble charts: stringency vs new cases per million, and new cases vs new deaths per million. Bubble size shows case fatality rate and color shows continent.

### 4️⃣ Ranking table
![Ranking table](assets/ranking_table.png)

Countries ranked by average new cases per million, with stringency, CFR, a case trend flag (increasing, decreasing, stable), and cumulative totals. A Top 10 view highlights the hardest-hit countries.

## Key findings

- By 2020-09-19 the data shows about **30.5 million** cumulative cases and **952 thousand** deaths worldwide, a crude case fatality rate of about **3.1%** (computed from the clean CSV).
- Average daily new cases per million differ sharply by continent: South America (about 48) is far above Asia (24), North America (22), Europe (20), Africa (5.5), and Oceania (4.5).
- Higher stringency did not always go with fewer cases. Timing, testing capacity, and population density change the picture.
- Small countries and territories show up as outliers because small populations inflate per-million values.

## Recommendations

- Judge countries on per-million and trend measures, not cumulative totals alone.
- Combine stringency with healthcare capacity and testing data before drawing policy conclusions.
- Extend the model with vaccination and post-2020 data for a longer view.

## Tools

Power BI Desktop · DAX · Power Query (M) · data modeling · time series · maps

## Files

```
Covid-19 Global Analysis/
├── COVID-19 Global Analysis.pbix
├── dataset before & after/    # raw and cleaned CSV
└── assets/                    # screenshots
```

## How to open

Open `COVID-19 Global Analysis.pbix` in Power BI Desktop and use the slicers and the page tabs.
