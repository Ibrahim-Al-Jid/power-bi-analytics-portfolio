<div align="center">

![Power BI Analytics Portfolio](assets/repo-banner.jpg)

# Power BI Analytics Portfolio

**Five complete business-intelligence projects, from raw data to a dashboard that supports a decision.**

🌐 **English** · [العربية](README.ar.md)

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=flat)
![Power Query](https://img.shields.io/badge/Power%20Query%20(M)-217346?style=flat)
![Projects](https://img.shields.io/badge/projects-5-blue?style=flat)
![Languages](https://img.shields.io/badge/docs-EN%20%7C%20AR-informational?style=flat)
![License](https://img.shields.io/badge/license-MIT-lightgrey?style=flat)

[Projects](#projects) · [Approach](#how-each-project-is-built) · [Skills](#skills-demonstrated) · [Open a project](#how-to-open-a-project)

</div>

---

## What this is

A portfolio of five Power BI projects by **Ibrahim Hamdy**. Each project answers a clear business question and ships with everything needed to check the work: the `.pbix` file, the data, dashboard screenshots, and a README that explains the questions, the data, the findings, and the recommendations.

Every README is available in English and Arabic. Numbers quoted in the READMEs were recomputed from the data files in this repository.

## Projects

<table>
<tr>
<td width="50%" valign="top">

### 🎵 [Spotify Streaming Analysis](Spotify%20Streaming%20Analysis/README.md)
*Music analytics · 4-page report*

Who dominates the daily Top-50 chart, and how do release type and explicit content differ?

**27,800** chart entries · **343** artists · May 2023 to Nov 2024

[English](Spotify%20Streaming%20Analysis/README.md) · [العربية](Spotify%20Streaming%20Analysis/README.ar.md)

<img src="Spotify%20Streaming%20Analysis/assets/OverView.png" alt="Spotify dashboard overview">

</td>
<td width="50%" valign="top">

### 🌍 [COVID-19 Global Analysis](Covid-19%20Global%20Analysis/README.md)
*Healthcare · 4-page report*

How did the first nine months of the pandemic unfold, and did stricter policy go with better outcomes?

**44K** daily country records · **210** countries · Dec 2019 to Sep 2020

[English](Covid-19%20Global%20Analysis/README.md) · [العربية](Covid-19%20Global%20Analysis/README.ar.md)

<img src="Covid-19%20Global%20Analysis/assets/overview.png" alt="COVID-19 dashboard overview">

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 👟 [Adidas Sales Dashboard](Adidas%20Sales%20Dashboard/README.md)
*Retail · one-page executive view*

How large is net revenue, what do discounts cost, and which categories and cities drive sales?

**$190.4M** net sales · 2016 to 2018

[English](Adidas%20Sales%20Dashboard/README.md) · [العربية](Adidas%20Sales%20Dashboard/README.ar.md)

<img src="Adidas%20Sales%20Dashboard/assets/dashboard.png" alt="Adidas sales dashboard">

</td>
<td width="50%" valign="top">

### 🛒 [Retail Sales Performance, Q1 2019](Retail-Sales-Performance-Q1-2019/README.md)
*Retail · one-page report*

How did a three-branch supermarket chain perform, and where does revenue come from?

**1,000** invoices · 3 branches · 6 product lines

[English](Retail-Sales-Performance-Q1-2019/README.md) · [العربية](Retail-Sales-Performance-Q1-2019/README.ar.md)

<img src="Retail-Sales-Performance-Q1-2019/assets/dashboard.png" alt="Retail sales dashboard">

</td>
</tr>
<tr>
<td colspan="2" valign="top">

### 📦 [Item Sales Performance Analysis](Item-Sales-Performance-Analysis/README.md)
*Sales and operations · star-schema model*

Which items and states drive sales and profit, and how concentrated is revenue?

**$19.9M** sales · **49.9%** profitability · 26,397 sales lines · 2013 to 2016

[English](Item-Sales-Performance-Analysis/README.md) · [العربية](Item-Sales-Performance-Analysis/README.ar.md)

<img src="Item-Sales-Performance-Analysis/assets/report.png" alt="Item sales report" width="60%">

</td>
</tr>
</table>

## Projects at a glance

| Project | Domain | Grain of the data | Pages | Modeling |
|---------|--------|-------------------|-------|----------|
| Spotify Streaming Analysis | Music | One song at one chart position per day | 4 | Single table, cleaned from a raw file |
| COVID-19 Global Analysis | Healthcare | One country per day | 4 | Single table with derived trend and fatality measures |
| Adidas Sales Dashboard | Retail | Sales by year, city, category | 1 | Embedded model |
| Retail Sales Performance Q1 2019 | Retail | One invoice | 1 | Single table |
| Item Sales Performance Analysis | Sales and operations | One sales line | 1 | Star schema (1 fact, 5 dimensions) |

## How each project is built

1. **Question first.** Each README starts from the business questions the dashboard must answer.
2. **Prepare the data** in Power Query (M): fix types, handle blanks and duplicates, remove aggregate rows, add derived columns. The Spotify and COVID-19 projects keep the raw and cleaned files side by side so the cleaning step can be checked.
3. **Model** the tables and relationships, then write **DAX** measures for the KPIs.
4. **Design** the report for a reader: KPIs on top, one idea per visual, filters where decisions are made.
5. **Conclude.** Each README ends with findings computed from the data and recommendations a manager could act on.

## Skills demonstrated

| Area | Evidence in this repository |
|------|-----------------------------|
| Data cleaning | Raw vs cleaned Spotify and COVID-19 files; documented blanks, duplicates, and aggregate rows |
| Data modeling | Star schema in the Item Sales project |
| DAX | KPI, profit, margin, fatality-rate, and trend measures |
| Visual design | Custom page navigation and backgrounds (Spotify), executive one-pager (Adidas), maps, Sankey, treemap, bubble charts |
| Analysis | Concentration of revenue, cross-country comparison, policy vs outcome, branch and product-line split |
| Communication | Plain-language findings and recommendations in two languages |

## Repository layout

```
power-bi-analytics-portfolio/
├── README.md · README.ar.md              this page, in English and Arabic
├── LICENSE
├── assets/                               banner image
├── Spotify Streaming Analysis/
├── Covid-19 Global Analysis/
├── Adidas Sales Dashboard/
├── Retail-Sales-Performance-Q1-2019/
└── Item-Sales-Performance-Analysis/
    each project folder holds: README.md · README.ar.md · .pbix · data · assets
```

## How to open a project

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows).
2. Download or clone this repository.
3. Open the `.pbix` file in the project folder. If Power BI asks where the data is, point it to that project's data folder.

## Data notes

- The datasets come from public sources and sample sets, and are used here for learning and demonstration. They belong to their original publishers.
- COVID-19 data: [Our World in Data](https://github.com/owid/covid-19-data), licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The cleaned file in this repository is derived from it.
- The Adidas dashboard is a practice project with Adidas styling. Its data is embedded in the `.pbix` and is not company data.
- The Retail data contains one invoice with an invalid date. The report drops it, and the project README explains how this affects the totals.

## License

Released under the [MIT License](LICENSE).
