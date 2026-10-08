# App Insights Unlocked: Google Play Store Analytics with Tableau

An end-to-end data analytics, business intelligence, and executive storytelling project built entirely with Tableau Public analyzing market dynamics across 9,638 unique applications and 37,427 cleaned user reviews from the Google Play Store.

---

## Executive Summary

Mobile app developers and tech enterprises face intense competition on digital storefronts. To guide product development, marketing, and monetization, this project decodes the quantitative and qualitative drivers of mobile application success, identifying critical adoption thresholds, pricing constraints, and user sentiment patterns.

---

## Key Metrics Summary

* **Total Applications Analyzed:** 9,638 unique apps
* **Total Cleaned User Reviews:** 37,427 non-null reviews
* **Platform Average Rating:** **4.17 out of 5 stars**
* **Unique Categories:** 33 categories
* **Monetization Split:** 92.19% Free vs. 7.81% Paid apps
* **High-Satisfaction Volume:** 6,280 apps rated $\ge 4.0$

---

## Repository Structure
.
├── Cleaned_Data/
│   ├── Executive_Theme.json                   # Visual design tokens & executive color palette
│   ├── googleplaystore_cleaned.csv            # 9,638 deduplicated apps with parsed numeric fields

│   └── googleplaystore_user_reviews_cleaned.csv# 37,427 non-null reviews with sentiment polarity

├── Raw_Data/

│   ├── googleplaystore.csv                    # Original raw Kaggle apps file (Read-only)

│   └── googleplaystore_user_reviews.csv       # Original raw Kaggle reviews file (Read-only)

├── Workbook/

│   └── Google Play Store - App Insights Workbook.twbx # Tableau packaged workbook

├── App_Insights_Executive_Story.pdf           # 5-page publication-grade PDF Executive Presentation

├── Case_Study_Document.md       # Formal case study, data dictionary & objectives

├── Complete_Solution_Guide.md   # Complete answers & Tableau steps for all 25 questions

└── README.md                                  # Project overview and navigation

---

## Categorized Deep Insights

### 1. The Scale-Satisfaction Law
* Average rating climbs monotonically from **3.95 stars** (<10k installs) to **4.28 stars** (10M+ installs). High satisfaction is mandatory to scale in the marketplace.

### 2. The Sizing Sweet Spot (15 MB – 35 MB)
* Apps in the 15-35 MB envelope achieve peak median installs (~19M). Apps >50 MB face steep download abandonment due to data friction.

### 3. The Freemium Monopoly (92.2% Share)
* Free apps generate **26.7x more user reviews** than paid apps. Upfront prices above $4.99 create sharp acquisition resistance and lower star ratings.

### 4. Sentiment Polarity as an Early Warning Signal
* High-rated apps ($\ge 4.5$ stars) average **+0.29 polarity**; sub-3.5 star apps drop to **+0.04**. Polarity collapse precedes star rating drops.

### 5. High-Demand Categories & Volume Champions
* Top demand categories by installs are dominated by **GAME** (13.3B), **COMMUNICATION** (11.0B), and **TOOLS** (7.9B), while review volume is heavily concentrated in social applications like Facebook, WhatsApp, and Instagram.

---

## Strategic Recommendations for Product & Growth Leadership

1. **Optimize Application Footprint (Size Management):**
   * Target the 15 MB to 35 MB delivery window to avoid download friction and maximize median install potential.
2. **Prioritize Free-to-Play/Freemium Monetization Models:**
   * Leverage free models to capture high review volume and user acquisition scale, reserving paid tiers ($0.99–$2.99 sweet spot) for niche utility apps.
3. **Monitor Sentiment Polarity Proactively:**
   * Track user sentiment polarity shifts as an early warning indicator before aggregate star ratings begin to decline.
4. **Focus Engineering Quality on High-Demand Verticals:**
   * Align feature releases and performance optimization with high-demand categories such as Games, Communication, and Tools.
