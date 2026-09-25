# 🚆 Indian Railways — Train Operations Analytics Report

*Compiled from the four-level data-engineering pipeline (Levels 1–4).*

## Executive Summary

- The network covers **11,113 train services** across **921 source** and
  **924 destination stations** (11,113 weekly records).
- Demand is stable across the week (**1,503–1,649 services/day**);
  **Friday** peaks and **Monday** is the quietest day.
- Operations are hub-driven: **CST-MUMBAI, SEALDAH, CHENNAI BEACH** lead, and the top-10 hubs carry
  **23.1%** of services. The busiest corridor is **CHENNAI BEACH <-> TAMBARAM**
  (274 services).
- Data quality is production-grade after the pipeline: **0 missing values**,
  1,153 corrupted day tokens repaired, station names standardized.

## 1 · Data Overview & Quality (Level 1–2)

| Metric | Value |
|--------|-------|
| Weekly records | 11,113 |
| Missing values after cleaning | 0 |
| Corrupted day tokens repaired | 1153 |
| Weekend / Weekday share | 28.8% / 71.2% |

## 2 · Network & Station Patterns (Level 2 + 4.1)

![Top stations](fig4_trains_per_station.png)

- **CST-MUMBAI** is the largest origin hub (513 trains).
- Busiest single route: **TAMBARAM -> CHENNAI BEACH** (137 services).

## 3 · Weekly Rhythm (Level 3 + 4.1)

![Weekly line](fig4_weekly_line.png)

- Correlation of volume with day position: **r=+0.381** (weak);
  weekend effect **r=+0.127** (negligible) — demand is evenly spread.

![OD heatmap](fig4_od_heatmap.png)

## 4 · Executive Dashboard (4.1)

![Dashboard](fig4_executive_dashboard.png)

## 5 · Recommendations

1. Keep reserve capacity for **Friday** peaks; schedule maintenance on **Monday**.
2. Protect weekend frequency — weekends carry **28.8%** of weekly volume.
3. Prioritize infrastructure & punctuality monitoring at **CST-MUMBAI, SEALDAH, CHENNAI BEACH**.
4. Optimize at route/corridor level — calendar day explains little of the variance.

---
*Generated automatically by `level4/level4_visualization_and_reporting.ipynb`.*
