# 🎵 Spotify Streaming Analysis

🌐 **English** | [العربية](README.ar.md) · [← Back to portfolio](../README.md)

An interactive four-page Power BI dashboard on Spotify's daily Top-50 chart: which artists and songs stay on top, how popularity relates to output, and how release type and explicit content differ.

![Overview](assets/OverView.png)

## Business questions

- Which artists dominate the chart, and by how much?
- Do artists with more songs on the chart also have higher popularity?
- How do albums, singles, and compilations compare?
- How much of the chart is explicit content?
- Are there release-month patterns?

## Dataset

| Item | Value |
|------|-------|
| File | `Data/spotify.csv` (clean), `Data/spotify_dirty.csv` (raw, kept to show the cleaning step) |
| Grain | One row = one song at one chart position on one day |
| Rows | 27,800 (clean) |
| Period | 2023-05-18 to 2024-11-27 |
| Distinct artists / songs | 343 / 794 |
| Columns | date, position, song, artist, popularity, duration_ms, album_type, total_tracks, release_date, is_explicit, album_cover_url |

**Cleaning.** The raw file has 5,581 blank song names, 5,589 blank artists, 5,563 blank popularity values, and 99 duplicate rows. These were fixed in Power Query to produce the clean file.

## Dashboard pages

| Page | What it shows |
|------|---------------|
| 🏠 Home | Navigation hub between the pages |
| 1️⃣ Overview | Chart entries, artist count, average popularity, album type split, explicit vs non-explicit |
| 2️⃣ Artists | Songs per artist, #1 hits, popularity vs productivity, average tracks per album |
| 3️⃣ Songs | Popularity by artist, distinct songs by year, popularity by album type and release date, tracks by month |

![Home](assets/Home.png)
![Artists](assets/Artists.png)
![Songs](assets/Songs.png)

## Key findings (computed from the clean CSV)

- **Taylor Swift** has 1,871 chart entries, more than double the next artist (Billie Eilish, 860).
- Most days a different artist takes #1. The most #1 days: Lady Gaga & Bruno Mars (77), Jung Kook & Latto (69), Sabrina Carpenter (51).
- **62%** of entries are album tracks, **38%** singles, under 1% compilations.
- **40%** of chart entries are explicit.
- Average popularity of chart entries is about **89.6**; the average chart song lasts about **3.3 minutes**.

> Note: the dashboard header shows slightly different headline numbers (for example 28K songs, 336 artists). The 28K figure counts chart entries, not distinct songs. The exact figures above come straight from the CSV.

## Recommendations

- Track the artists with the most chart entries as the benchmark: volume of simultaneous active songs, not one hit, drives presence on the chart.
- Use the Songs page to time releases against the months with the highest chart activity.
- Treat singles (38% of entries) and albums (62%) as different strategies and compare their popularity before choosing a release format.

## Tools

Power BI Desktop · DAX · Power Query (M) · custom page navigation and background design

## Files

```
Spotify Streaming Analysis/
├── spotify project .pbix     # dashboard
├── Data/                     # spotify.csv, spotify_dirty.csv
├── assets/                   # page screenshots
├── Backgrounds/              # page background designs
└── Icons/                    # navigation icons
```

## How to open

Open `spotify project .pbix` in Power BI Desktop. If asked, point the data source to `Data/spotify.csv`.
