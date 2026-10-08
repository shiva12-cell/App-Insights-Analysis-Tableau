# App Insights Unlocked: Google Play Store Analytics with Tableau

[![Tableau](https://img.shields.io/badge/Tableau-Public%202026.2-E97627?logo=tableau&logoColor=white)](https://public.tableau.com/)
[![Analysis](https://img.shields.io/badge/Analysis-Exploratory%20Data%20Analysis-1F77B4)](#key-analytical-findings)
[![Dataset](https://img.shields.io/badge/Dataset-Google%20Play%20Store-2CA02C?logo=googleplay&logoColor=white)](#dataset-specifications)
[![Deliverables](https://img.shields.io/badge/Deliverables-Case%20Study%20%26%20Solution%20Guide-9467BD)](#project-deliverables)

An end-to-end data analytics, business intelligence, and executive storytelling project built entirely with **Tableau Public** analyzing market dynamics across **9,638 unique applications** and **37,427 cleaned user reviews** from the Google Play Store.

---

##  Project Overview & Problem Statement

Mobile app developers and tech enterprises face intense competition on digital storefronts. To guide product development, marketing, and monetization, this project decodes the quantitative and qualitative drivers of mobile application success:

- **What factors distinguish high-performing applications ($10\text{M}+$ installs, rating $\ge 4.2\text{ ★}$) from stagnant products?**
- **How do file footprint (MB) and pricing strategies affect download adoption and churn?**
- **What qualitative user sentiment patterns explain the divide between satisfied and dissatisfied users?**

---

##  Key Analytical Findings

```
┌────────────────────────────────────────────────────────────────────────┐
│ 4 CORE MARKET REALITIES                                                │
├────────────────────────────────────────────────────────────────────────┤
│ 1. THE SCALE-SATISFACTION LAW                                          │
│    Average rating climbs monotonically from 3.95 ★ (<10k installs)     │
│    to 4.28 ★ (10M+ installs). High satisfaction is mandatory to scale. │
├────────────────────────────────────────────────────────────────────────┤
│ 2. THE SIZING SWEET SPOT (15 MB – 35 MB)                               │
│    Apps in the 15-35 MB envelope achieve peak median installs (~19M).  │
│    Apps >50 MB face steep download abandonment due to data friction.   │
├────────────────────────────────────────────────────────────────────────┤
│ 3. THE FREEMIUM MONOPOLY (92.2% SHARE)                                 │
│    Free apps generate 26.7x more user reviews than paid apps. Upfront  │
│    prices above $4.99 create sharp acquisition resistance and lower ★. │
├────────────────────────────────────────────────────────────────────────┤
│ 4. SENTIMENT POLARITY AS AN EARLY WARNING SIGNAL                       │
│    High-rated apps (≥4.5 ★) average +0.29 polarity; sub-3.5 ★ apps     │
│    drop to +0.04. Polarity collapse precedes star rating drops.        │
└────────────────────────────────────────────────────────────────────────┘
```

---

##  Tableau Dashboard Suite Architecture

The analytical suite is structured across **3 executive dashboards** following the theme specified in `Cleaned_Data/Executive_Theme.json`:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ 1. DB1_Market_Overview (Executive Macro View)                                          │
│    • KPI Tier: Platform Avg Rating (4.17 ★), Unique Categories (33), Apps ≥ 4.0 (6,280)│
│    • Top 5 Demand Categories by Installs: GAME (13.3B), COMM (11.0B), TOOLS (7.9B)     │
│    • Monetization Split: Free (92.19%) vs. Paid (7.81%)                                │
│    • Audience Content Rating Distribution: Everyone (81.8%), Teen (10.7%)              │
│    • 1 Billion+ Installs Leaderboard                                                   │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 2. DB2_Product_Dynamics (Engineering & Pricing Optimization)                           │
│    • App Size Distribution: Right-skewed histogram (Peak at 5-20 MB)                   │
│    • Size vs. Average Installs: Proving the 15-35 MB scale envelope                    │
│    • Paid App Price Elasticity: Sweet spot at $0.99 – $2.99 (4.26 ★)                   │
│    • Highest Rated Categories: EVENTS (4.44 ★), ART & DESIGN (4.36 ★), EDUCATION (4.36)│
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 3. DB3_Sentiment_and_Growth (Customer Experience & Lifecycle)                          │
│    • Review Sentiment Breakdown: Positive (64.1%), Neutral (13.8%), Negative (22.1%)  │
│    • Binned Install vs. Rating Progression: From 3.95 ★ up to 4.28 ★                   │
│    • Review Volume Champions: Facebook (78M), WhatsApp (69M), Instagram (66M)         │
│    • Release Velocity Timeline: Exponential update surge into mid-2018 (6,270 apps)    │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

##  Repository & Directory Structure

```text
├── App_Insights_Executive_Story.pdf           # 5-page publication-grade PDF Executive Presentation
├── Case_Study_Document.md       # Formal case study, data dictionary & objectives
├── Complete_Solution_Guide.md   # Complete answers & Tableau steps for all 25 questions
├── README.md                                  # Project overview and navigation
├── Cleaned_Data/
│   ├── Executive_Theme.json                   # Visual design tokens & executive color palette
│   ├── googleplaystore_cleaned.csv            # 9,638 deduplicated apps with parsed numeric fields
│   └── googleplaystore_user_reviews_cleaned.csv# 37,427 non-null reviews with sentiment polarity
├── Raw_Data/
    ├── googleplaystore.csv                    # Original raw Kaggle apps file (Read-only)
    └── googleplaystore_user_reviews.csv       # Original raw Kaggle reviews file (Read-only)


---

##  25 Challenge Questions Index

All 25 questions from `App Insights (Tableau).pdf` are solved and documented in [`Deliverable_2_Complete_Solution_Guide.md`](./Deliverable_2_Complete_Solution_Guide.md):

| Tier | Questions Covered |
| :--- | :--- |
| **Basic (1 – 10)** | Average Rating Benchmark (`4.17 ★`), Category Count (`33`), Size Distribution (Histogram), Free vs. Paid Split (`92.2%`), Prevalent Content Rating (`Everyone: 81.8%`), Top 5 Most Installed Apps (`1B+ Club`), High-Satisfaction Volume (`6,280 apps ≥ 4.0`), Reviews Free vs. Paid (`26.7x ratio`), Avg Size by Category (`Game: 44.3MB`), Maintenance Velocity in 2018 (`6,270 apps`). |
| **Medium (1 – 10)** | Rating vs. Installs Correlation ($r \approx +0.052$), Highest-Rated Categories (`Events: 4.44 ★`), Paid Price Elasticity ($0.99–$2.99 peak), Content Rating Variance (Box-and-Whisker), Top 1M+ Install Genres (`Tools`, `Action`), Maintenance Frequency & Decay, Size vs. Download Volume, Global Review Champions, Demographic Splits, Top 5 Cumulative Install Categories. |
| **Advanced (1 – 5)**| The "Perfect Rating Trap" (Small-sample 5.0 ★ bias), Time-Series Update Velocity (Seasonal I/O spikes), Binned Install Progression ($3.95 \to 4.28\text{ ★}$), Review Sentiment Polarity across rating tiers, Genre Satisfaction Stability (Mean vs. Median ratings). |

---


