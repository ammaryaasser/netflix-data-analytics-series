# 🎬 Netflix End-to-End Business Intelligence & Analytics Series

<p align="center">
  <img src="assets/Netflix_Logomark.png" alt="Netflix Logo" width="100%"/>
</p>

## 📌 Project Overview
This repository contains a comprehensive **6-Part End-to-End Netflix Data Analytics Project**. The project simulates a real-world business intelligence workflow—starting from raw data ingestion and advanced ETL cleaning, all the way to building multi-page executive dashboards and strategic data models.

---

## 🛣️ Project Roadmap & Architecture

The repository is structured around a progressive 6-stage analytics lifecycle:

| Stage | Task Name | Level | Core Focus & Deliverables | Status |
| :---: | :--- | :---: | :--- | :---: |
| **Task 1** | **Data Preparation & Power BI Setup** | Easy | Data profiling, fixing line breaks, locale date conversions, deduplication, handling missing values, and building a normalized Star-Schema model[cite: 2, 3]. | ✅ Completed |
| **Task 2** | **Netflix Content Overview Dashboard** | Easy | Multi-page interactive dashboard, core KPI tracking, content distribution analysis, and movie vs. TV show comparison[cite: 15, 16]. | ✅ Completed |
| **Task 3** | **Global Content Insights Dashboard** | Medium | Geographic analysis, map charts, drill-down reports, and regional content volume rankings. | ⏳ Upcoming |
| **Task 4** | **Content Growth & Trend Analysis** | Medium | Time-series modeling, release year trends, yearly growth tracking, and trend indicators using DAX. | ⏳ Upcoming |
| **Task 5** | **Audience & Content Category Intelligence** | Advanced | Audience rating segmentation, category performance visuals, advanced DAX measures, and executive reporting. | ⏳ Upcoming |
| **Task 6** | **Executive Business Intelligence Solution** | Advanced | Consolidating business metrics, multi-page dashboard architecture, drill-through reports, and strategic recommendations. | ⏳ Upcoming |

---

## 📊 Summary of Completed Tasks

### Task 1: Data Preparation & ETL Workflow (Power Query)
* **Data Cleansing:** Resolved quoted line break errors (record `s8420`), applied locale-aware English (United States) date parsing, trimmed whitespace, and purged duplicates (reducing total catalog count from 8,790 to 8,786 rows)[cite: 2, 3].
* **Missing Value Treatment:** Replaced `"Not Given"` string placeholders in `director` and `country` with `"Unknown"`[cite: 2].
* **Data Modeling:** Normalized multi-valued attributes into separate dimension tables (`Genres` and `Directors`) and established a clean **Star Schema** connected to the `Titles` fact table[cite: 3].
* **Validation:** Implemented strict row validation using `DISTINCTCOUNT(show_id)` to ensure accurate aggregate metrics across overlapping genre categories[cite: 3].

---

### Task 2: Netflix Content Overview Dashboard (2-Page Executive Report)

#### Page 1: Catalog Overview
* **Headline Metrics (KPIs):** Total Catalog Titles (**8,786**), Total Movies (**6,123**), Total TV Shows (**2,663**), Top Country (**United States**), and Top Genre (**International Movies**)[cite: 15].
* **Temporal Growth & Top Producers:** Line chart tracking catalog additions from 2008–2021 alongside horizontal bar charts ranking top producing countries (US: 3.2K, India: 1.1K, UK: 0.6K)[cite: 15].
* **Genre & Target Audience Distribution:** Visual breakdown of primary genres and target demographic groups (Adults: 4.0K, Teens: 2.6K, Kids: 2.1K)[cite: 15].
* **Content Breakdown:** Donut chart illustrating the catalog split (**70% Movies vs. 30% TV Shows**)[cite: 15].

#### Page 2: Movies vs. TV Shows Comparative Analysis
* **Core Comparison Metrics:** Average Movie Length (**99.6 Min**), Average TV Seasons (**1.8 Seasons**), Average Release Year (**Movies 2013 \| TV 2017**), and Addition Speed indicators[cite: 16].
* **Shifting Strategy Analysis:** Comparative stacked bar chart tracking annual release trends between Movies and TV Shows to identify strategic portfolio shifts over time[cite: 16].
* **Duration & Season Granularity:** Grouped bar charts segmenting movie runtimes (Under 90 min, 90–120 min, Over 120 min) and TV show season longevity (1 Season vs. 2+ Seasons)[cite: 16].
* **Interactive Navigation & Slicers:** Full navigation control with interactive slicers for Country, Audience rating, Release Year range sliders, and a one-click **Reset Filters** button[cite: 15, 16].

---

## 📁 Repository Structure

```text
├── README.md                              <-- Master project overview & roadmap
├── Task 1/
│   ├── Task 1 - Documentation.pdf         <-- Detailed ETL and data cleaning decisions[cite: 2]
│   └── Task 1 - Netflix data prep.pbix    <-- Power BI data model file[cite: 4]
├── Task 2/
│   └── Netflix Content Overview.pbix      <-- Multi-page Power BI dashboard[cite: 5]
└── assets/                                <-- High-resolution UI screenshots & diagrams
