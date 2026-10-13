# 🎬 Netflix End-to-End Data Analytics Series (Task 1: Data Cleaning & Modeling)

## 📌 Project Overview
This repository represents **Task 1 (Data Preparation & Power BI Setup)** of a **6-Part End-to-End Netflix Business Intelligence Project** powered by **Auspify**. 

The goal of this foundational phase is to transform raw, unformatted Netflix catalog data into a clean, normalized, and validated **Star-Schema Data Model** in Power Query, laying the ground truth for all subsequent dashboards and analytical tasks.

---

## 🛣️ The 6-Task Netflix Project Roadmap

- [x] **Task 1: Data Preparation & Power BI Setup** *(Current Repository)*
- [x] **Task 2: Netflix Content Overview Dashboard**
- [ ] **Task 3: Global Content Insights Dashboard**
- [ ] **Task 4: Content Growth & Trend Analysis**
- [ ] **Task 5: Audience & Content Category Intelligence Dashboard**
- [ ] **Task 6: Executive Business Intelligence Dashboard**

---

## 🔍 Data Problems & ETL Cleaning Decisions (Power Query)

During initial data profiling, several critical data anomalies were identified and resolved:

| # | Data Problem Identified | Cleaning Decision & Transformation |
|---|-------------------------|-----------------------------------|
| 1 | **Quoted Line Break Error** | Fixed record `s8420` (*The Memphis Belle*), which contained an embedded line feed causing line splits and `TV-PG` date errors. Set source to *Ignore quoted line breaks* and replaced line feeds with spaces. |
| 2 | **Text Dates under Regional Settings** | Converted `date_added` from text (`M/D/YYYY`) to `Date` data type using `Change Type with Locale (English, United States)` to avoid parsing conflicts in non-US locales. |
| 3 | **Hidden Whitespace** | Applied `Trim` to all text columns prior to deduplication. |
| 4 | **Duplicates under Unique IDs** | Identified duplicate titles with distinct `show_id` values (`15-Aug`, `22-Jul`, `9-Feb`, `Consequences`). Removed duplicates across all fields except `show_id`, reducing total rows from **8,790 to 8,786**. |
| 5 | **Fake Blanks ("Not Given")** | Replaced `"Not Given"` string placeholders in `director` (2,587 rows) and `country` (287 rows) with `"Unknown"` instead of dropping records. |
| 6 | **Mixed Unit Durations** | Split `duration` into numerical `duration_value` and categorical `duration_unit` (`min` vs. `Season`). |
| 7 | **Multi-Valued Comma-Separated Columns** | Normalized `listed_in` (genres) and `director` into separate dimension tables (`Genres` and `Directors`) using *Split Column by Delimiter into Rows* to enable accurate count metrics. |
| 8 | **Derived Columns** | Created `year_added`, `month_added`, and `rating_group` (*Kids, Teens, Adults, Unrated*). |

---

## 📐 Data Model & Validation

* **Schema Type:** Star Schema (Fact table `Titles` linked to `Genres` and `Directors` dimensions via `show_id` with 1-to-Many bidirectional filtering).
* **Validation Logic:** Created DAX validation measures using `DISTINCTCOUNT(show_id)` to ensure multi-genre titles are not overcounted.
* **Final Verified Row Count:** **8,786 Titles** (6,123 Movies | 2,663 TV Shows).

