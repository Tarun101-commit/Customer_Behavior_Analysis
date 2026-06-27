# Customer_Behavior_Analysis
Data Analysis Project Showcasing customer bahavior analysis using Pandas, SQL and Power BI
## Project Overview
[cite_start]This end-to-end data analytics project investigates customer purchasing patterns using a transactional dataset of **3,900 purchases** across **18 key features**[cite: 3, 7]. [cite_start]The primary objective is to uncover high-impact insights into spending behavior, demographic segments, product choices, and subscription dynamics to drive data-backed strategic business decisions[cite: 4].

[cite_start]The project showcases a complete data pipeline engineering workflow: **Data Extraction & Preprocessing (Python) ➡️ Database Migration (PostgreSQL) ➡️ Advanced Business Querying (SQL) ➡️ Interactive Dashboarding (Power BI)**[cite: 14, 23, 24, 36].

---

## Technical Stack & Tools
* [cite_start]**Data Processing:** Python (`pandas`, `numpy`) [cite: 15]
* [cite_start]**Database Management:** PostgreSQL [cite: 23]
* [cite_start]**Business Intelligence:** Power BI [cite: 36]
* **Documentation & Version Control:** Git & Markdown

---

## Data Pipeline & Implementation

### 1. Exploratory Data Analysis & ETL (Python)
* [cite_start]**Initial Audit:** Conducted structural analysis using `df.info()` and statistical summaries via `df.describe()` to map out numerical distributions[cite: 16].
* [cite_start]**Imputation Strategy:** Detected 37 missing data points in the `Review Rating` column[cite: 12]. [cite_start]Imputed them granularly using the **median rating of their respective product categories** to avoid data skewing[cite: 17].
* [cite_start]**Data Hygiene & Engineering:** * Standardized column naming conventions to uniform `snake_case`[cite: 18].
    * [cite_start]Binned continuous customer ages into categorical `age_group` variables[cite: 20].
    * [cite_start]Transformed purchase frequency granularities into a quantitative `purchase_frequency_days` metric[cite: 21].
* [cite_start]**Redundancy Elimination:** Cross-verified collinearity between `discount_applied` and `promo_code_used`, safely dropping the redundant `promo_code_used` column[cite: 22].
* [cite_start]**Database Integration:** Automated the transfer of the fully cleaned DataFrame into a structured PostgreSQL production database for deep SQL analysis[cite: 23].

### 2. Structured Data Analysis (PostgreSQL)
A series of complex SQL queries were written to extract precise operational and financial metrics:

* [cite_start]**Gender Financial Split:** Analyzed macro revenue generation by customer sex[cite: 26].
* [cite_start]**High-Value Discount Profiling:** Identified high-spending customers who leverage discounts but still hold an average purchase value above the global baseline[cite: 27].
* [cite_start]**Product Performance Mapping:** Extracted the top 5 highest-rated products across all categories to identify quality leaders[cite: 28].
* [cite_start]**Logistics Impact Study:** Measured variations in average cart sizes based on selected shipping types (`Express` vs. `Standard`)[cite: 29].
* [cite_start]**Subscription Value Analysis:** Compared total revenue volume and average transaction sizes between subscriber and non-subscriber cohorts[cite: 30].
* [cite_start]**Markdown Elasticity Index:** Identified items possessing the highest percentage of discount-dependent transactions[cite: 31].
* [cite_start]**RFM-Style Customer Segmentation:** Grouped the consumer ecosystem into `New`, `Returning`, and `Loyal` cohorts based on historical purchasing counts[cite: 32].

---

## Data Insights & Business Value Realized

### Financial & Operational Metrics (SQL Outputs)

| Metric Evaluated | Category / Dimension | Key Insight / Value |
| :--- | :--- | :--- |
| **Revenue by Gender** | Male vs. Female | **Male:** $157,890 \| [cite_start]**Female:** $75,191 *(Males drive >2x revenue)* [cite: 26, 38] |
| **Shipping Behavior** | Express vs. Standard | **Express Avg:** $60.48 \| [cite_start]**Standard Avg:** $58.46 [cite: 29, 39] |
| **Subscription Value** | Non-Subscribers vs. Subscribers | **No:** 2,847 customers ($170,436) \| [cite_start]**Yes:** 1,053 customers ($62,645) [cite: 30] |
| **Top 5 Rated Products** | Item Performance | 1. Gloves (3.86) \| 2. Sandals (3.84) \| 3. Boots (3.82) \| 4. Hat (3.80) \| 5. [cite_start]Handbag (3.78) [cite: 28] |
| **Discount Dependency** | Core Markdown Items | **Hats:** 50.00% \| **Sneakers:** 49.66% \| [cite_start]**Coats:** 49.07% *(Highly discount-dependent)* [cite: 31, 43] |
| **Customer Segments** | Retention Tracking | **Loyal:** 3,116 \| **Returning:** 701 \| [cite_start]**New:** 83 *(Heavy loyalty baseline)* [cite: 32, 45] |
| **Age Group Split** | Revenue Contributions | **Young Adult:** $62,143 \| **Middle Aged:** $59,197 \| **Adult:** $55,978 \| [cite_start]**Senior:** $55,763 [cite: 35] |

---

## Interactive Power BI Dashboard
[cite_start]An executive-ready dashboard was constructed to provide interactive filtering across `Subscription Status`, `Gender`, `Category`, and `Age Group` parameters[cite: 36].

* [cite_start]**KPI Blocks:** Dynamically displays total customer scale (3.9K), overall average purchase value ($59.76), and collective review rating baseline (3.75)[cite: 36].
* [cite_start]**Category Dynamics:** Visualizes total revenue distributions across lines, clearly showing `Clothing` leading macro market share, followed by `Accessories`, `Footwear`, and `Outerwear`[cite: 36, 41].
* [cite_start]**Demographic Layouts:** Tracks volumetric purchase transactions partitioned by specialized customer age distributions[cite: 36].

---

## Strategic Recommendations
1.  [cite_start]**Monetize High-Spending Male Cohorts:** Target the dominant male demographic ($157.89K in revenue) with dedicated up-sell campaigns designed to convert high-value one-time buyers into recurring ecosystem subscribers[cite: 38].
2.  [cite_start]**Optimize Shipping Thresholds:** Capitalize on higher express shipping order values ($60.48) by implementing an automated **Free Express Shipping on Orders Over $65** threshold to organically lift cross-category average order value (AOV)[cite: 39, 40].
3.  [cite_start]**Cross-Category Product Bundling:** Leverage high consumer sentiment on specific sub-items (Gloves, Sandals) by bundling them directly with high-volume, lower-rated core `Clothing` products to lift sluggish macro-category revenues[cite: 41, 42].
4.  [cite_start]**Mitigate Margin Markdown Erosion:** Phase out blanket flat-rate discounts on highly discount-dependent goods (Hats, Sneakers, Coats)[cite: 43, 44]. [cite_start]Replace them with conditional volume multi-buys or tiered loyalty point incentives to secure net profit margins[cite: 44].
5.  [cite_start]**Defend the Loyal Core Base:** Since the active business revenue is heavily anchored by **3,116 Loyal customers** versus only 83 New acquisitions, allocate the majority of retention capital toward exclusive loyalty experiences and high-tier perks[cite: 45, 46].
