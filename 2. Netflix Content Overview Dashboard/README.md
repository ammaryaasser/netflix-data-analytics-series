# 📊 Task 2: Netflix Content Overview Dashboard

![Task 2 Dashboard Overview](assets/dashboard_overview.png)

## 📌 Task Overview
Building upon the normalized Star Schema from Task 1, **Task 2** focuses on designing a professional, 2-page executive business intelligence dashboard[cite: 6]. This report delivers comprehensive library analytics, tracking high-level platform growth, regional content distributions, and deep comparative metrics between Movies and TV Shows.

---

## 📑 Dashboard Architecture & Report Structure

### Page 1: Catalog Overview & Library Demographics
* **Headline Metrics (KPIs):** Integrated top-line KPI cards tracking Total Catalog Titles (**8,786**), Total Movies (**6,123**), Total TV Shows (**2,663**), Top Country (**United States**), and Top Genre (**International Movies**).
* **Temporal Growth Trend:** Line chart mapping title additions chronologically from 2008 to 2021 to illustrate platform scaling velocity.
* **Geographic Breakdown:** Horizontal bar chart visualizing top content-producing countries led by the United States (3.2K) and India (1.1K).
* **Genre & Target Audience Segmentation:** Clear ranking of primary catalog genres alongside target demographic groups (Adults: 4.0K, Teens: 2.6K, Kids: 2.1K).
* **Format Share:** Donut visualization displaying the overarching content split (**70% Movies vs. 30% TV Shows**).

### Page 2: Movies vs. TV Shows Comparative Analysis
* **Core Comparison Metrics:** Advanced performance cards displaying Average Movie Length (**99.6 Min**), Average TV Seasons (**1.8 Seasons**), Average Release Year splits (**Movies 2013 | TV 2017**), and platform addition velocity metrics.
* **Strategic Portfolio Shift:** Stacked analytical bar charts tracking annual release trends across formats to evaluate platform pivot strategies toward episodic content.
* **Granular Duration & Season Distribution:** Grouped distribution charts evaluating movie runtimes (Under 90 min, 90–120 min, Over 120 min) versus TV show lifespan longevity (1 Season vs. 2+ Seasons).
* **Interactive Filtering Controls:** Global report slicers empowering users to filter seamlessly by Country, Audience rating, and Release Year ranges, supplemented by a dedicated **Reset Filters** action button.

    ├── dashboard_overview.png             <-- Page 1: Catalog Overview UI screenshot
    └── movies_vs_tv_shows.png             <-- Page 2: Comparative Analysis UI screenshot
