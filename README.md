# 🗳️ Tamil Nadu Assembly Elections 2026 — Data Analysis

> A constituency-level data analysis of the Tamil Nadu Legislative Assembly Elections 2026, benchmarked against the 2021 results — covering seat shifts, regional patterns, margin trends, and constituency-level flip behaviour across all **234 seats** and **32 districts**.

---

## 📁 Repository Structure

```
Tamil-Nadu-Elections-2026/
│
├── data/
│   └── TN_Elections_2026.xlsx          # Core dataset (2 sheets)
│
├── dashboard/
│   └── TN_Elections_2026.pbix          # Power BI interactive dashboard
│
├── presentation/
│   └── TN_2026_Election_Analysis.pptx  # 10-slide executive summary deck
│
└── README.md
```

---

## 📊 Data: `TN_Elections_2026.xlsx`

The workbook contains **2 sheets**:

### Sheet 1 — `winners 21 & 26`

One row per constituency (234 rows). The full column schema:

| Column | Description |
|---|---|
| `constituency` | Assembly constituency name |
| `ac_number` | Assembly constituency number (1–234) |
| `winners 2021.candidate` | Winning candidate name in 2021 |
| `winners 2021.party` | Winning party in 2021 |
| `winners 2021.votes` | Votes received by 2021 winner |
| `winners 2026.candidate` | Winning candidate name in 2026 |
| `winners 2026.party` | Winning party in 2026 |
| `winners 2026.votes` | Votes received by 2026 winner |
| `district` | District (32 districts covered) |
| `region` | One of 6 regions: Central, Chennai Metro, Delta, Kongu, North, South |
| `reserved` | Seat category — GEN (188), SC (44), ST (2) |
| `runner up 2021.candidate` | Runner-up candidate in 2021 |
| `runner up 2021.party` | Runner-up party in 2021 |
| `runner up 2021.votes` | Runner-up votes in 2021 |
| `runner up 2026.candidate` | Runner-up candidate in 2026 |
| `runner up 2026.party` | Runner-up party in 2026 |
| `runner up 2026.votes` | Runner-up votes in 2026 |
| `Margin votes 2021` | Winning margin in votes (2021) |
| `Margin votes 2026` | Winning margin in votes (2026) |
| `Total votes 2021` | Total valid votes polled (2021) |
| `Total votes 2026` | Total valid votes polled (2026) |
| `Margin % 2021` | Margin as % of total votes (2021) |
| `Margin % 2026` | Margin as % of total votes (2026) |
| `Flipped` | `Flipped` if the seat changed party; `Retained` if same party won |

### Sheet 2 — `Master_Seat_Comparison`

One row per Party × Region combination. Used for regional heatmaps and geographic analysis:

| Column | Description |
|---|---|
| `Helper_key` | Composite join key e.g. `Central_DMK` |
| `Region` | One of 6 regions |
| `Party` | Political party |
| `Seats_2021` | Seats won in 2021 |
| `Seats_2026` | Seats won in 2026 |
| `Change` | Net change (`Seats_2026 − Seats_2021`) |

---

## 📈 Key Findings

### Statewide Numbers

| Metric | Value |
|---|---|
| Total constituencies | 234 |
| Constituencies flipped | **163 (70%)** |
| Constituencies retained | 71 (30%) |
| Avg margin votes — 2021 | 22,871 |
| Avg margin votes — 2026 | **16,784 ↓ (~27% drop)** |
| Districts covered | 32 |

### Party Performance (2021 → 2026)

| Party | 2021 Seats | 2026 Seats | Change |
|---|---|---|---|
| **TVK** | 0 | **108** | **+108** |
| DMK | 133 | 59 | **−74** |
| AIADMK | 66 | 47 | −19 |
| INC | 11 | 5 | −6 |
| CPI(M) | 2 | 2 | 0 |
| CPI | 2 | 2 | 0 |
| PMK | 5 | 4 | −1 |
| VCK | 1 | 2 | +1 |
| BJP | 2 | 1 | −1 |
| IUML | 0 | 2 | +2 |
| AMMK | 0 | 1 | +1 |
| DMDK | 0 | 1 | +1 |

### Regional Flip Summary

| Region | Total Seats | Flipped | Retained | Flip Rate |
|---|---|---|---|---|
| Chennai Metro | 32 | 30 | 2 | **94%** |
| Kongu | 33 | 27 | 6 | 82% |
| North | 37 | 27 | 10 | 73% |
| South | 58 | 38 | 20 | 66% |
| Central | 41 | 26 | 15 | 63% |
| Delta | 33 | 15 | 18 | **45%** |

### TVK & DMK Net Seat Change by Region

| Region | TVK Gain | DMK Loss |
|---|---|---|
| Chennai Metro | +29 | −27 |
| South | +26 | −9 |
| Kongu | +16 | −1 |
| North | +15 | −15 |
| Central | +12 | −13 |
| Delta | +10 | −9 |

### Margin Distribution (2026)

| Category | Seat Count |
|---|---|
| Very Close (< 5%) | **103** |
| Competitive (5–10%) | 65 |
| Comfortable (10–20%) | 49 |
| Dominant (> 20%) | 17 |

### 10 Closest Contests — 2026

| Constituency | Winner Party | Margin (votes) |
|---|---|---|
| Tiruppattur | TVK | **1** |
| Veppanahalli | DMK | 138 |
| Kanniyakumari | AIADMK | 214 |
| Polur | TVK | 227 |
| Tirukkoyilur | AIADMK | 285 |
| Paramathi-Velur | AIADMK | 308 |
| Kulithalai | DMK | 579 |
| Kumbakonam | TVK | 679 |
| Palani | AIADMK | 693 |
| Tindivanam | VCK | 734 |

### 5 Biggest Wins — 2026

| Constituency | Winner Party | Margin (votes) |
|---|---|---|
| Edapadi | AIADMK | 98,110 |
| Shozhinganallur | TVK | 96,780 |
| Madavaram | TVK | 94,985 |
| Avadi | TVK | 76,311 |
| Salem (West) | TVK | 74,867 |

---

## 📊 Power BI Dashboard: `TN_Elections_2026.pbix`

The interactive dashboard is built on top of the Excel data and includes the following pages:

| Page | Key Visuals |
|---|---|
| **Geographic Analysis** | Regional seat shift bar chart (2021 vs 2026), Party × Region net change heatmap |
| **Flip Analysis** | Sankey diagram (party-to-party flow), Flipped vs Retained donut chart, Region-wise flip count bar chart |
| **Margin Analysis** | % Margin distribution bar chart, Closest contests table, Avg margin KPI cards (22.87K vs 16.78K) |

**Tool:** Microsoft Power BI Desktop  
**Data source:** `TN_Elections_2026.xlsx` (direct connection)

---

## 📑 Presentation Deck: `TN_2026_Election_Analysis.pptx`

A 10-slide executive summary prepared for AtliQ Media:

| Slide | Title |
|---|---|
| 1 | Tamil Nadu 2026 Election: A Data Story |
| 2 | Methodology |
| 3 | Statewide Snapshot |
| 4 | Regional voting patterns diverged sharply across Tamil Nadu |
| 5 | Geographic Deep Dive (Chennai Metro · Central · Delta) |
| 6 | A large share of constituencies changed hands in 2026 |
| 7 | Flip Geography |
| 8 | Many seats were decided by narrow margins |
| 9 | Key Takeaways |
| 10 | Closing |

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| Microsoft Excel | Data preparation and seat comparison tables |
| Power BI Desktop | Interactive dashboard and all visualizations |
| PowerPoint | Executive presentation deck |
| ECI Portal | Primary public data source |

---

## ⚠️ Disclaimer

All data is sourced exclusively from the **Election Commission of India (ECI)** public portal. This analysis is strictly non-partisan and is intended solely for informational and educational purposes. No affiliation with any political party, candidate, or campaign.

---

## 🙋 About

Prepared by the **Pavithra CY, Aspiring Data Analyst** as part of the Tamil Nadu 2026 post-election analysis series.

