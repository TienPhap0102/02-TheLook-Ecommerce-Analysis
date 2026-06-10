# 📊 The Look eCommerce: Comprehensive Health Assessment & Long-Term Growth Strategy

## 📌 Executive Summary & Business Context
This project conducts a comprehensive business health assessment of The Look eCommerce platform. The main objective is to identify operational inefficiencies, evaluate customer behavior, analyze retention performance, and propose data-driven strategies to improve long-term business growth.

The analysis focuses on several key areas, including customer conversion, retention, revenue distribution, product performance, market basket behavior, and inventory risk. Based on the findings, this project provides actionable recommendations to improve Customer Lifetime Value (LTV), reduce revenue leakage, and increase Average Order Value (AOV).

**The project aims to answer the following business questions:**

* Where are users dropping off in the customer journey?
* Is the platform successfully retaining customers after their first purchase?
* Which product categories generate the majority of revenue?
* What product combinations can be used for cross-selling strategies?
* Which customer segments should be prioritized for retention and win-back campaigns?
* How can the business optimize inventory and reduce return/cancellation risks?

---

## 2. 📂 Dataset Overview & Data Quality
[cite_start]The project utilizes **The Look eCommerce** dataset, a multi-million-row dataset capturing the comprehensive lifecycle of e-commerce operations, from user web traffic events to final product purchases and deliveries[cite: 3, 13].

### Data Volume & Scale:
* **Total Events:** 2M+ records tracking granular user interactions and behaviors on the platform
* **Total Orders:** 127,194 completed transactions
* **Total Users:** 100K unique customers mapped across the platform
* **Total Products:** 29K+ unique SKUs distributed across 26 distinct product categories

### Data Quality & Audit (Overall Health Score: ~95%):
* **Uniqueness:** Zero duplicate records were found within the primary transaction tables, ensuring a single source of truth for all financial and order-level analysis.
* **Consistency:** Missing or null values are logically sound and strictly aligned with the systematic order lifecycle status transitions (e.g., cancellation or return timestamps).

### Technical Pre-processing & Engineering:
* **Temporal Standardization:** Stripped 'UTC' suffixes and cast temporal columns into the proper `datetime` format to ensure precise time-series and cohort analysis.
* **Outlier Management:** Identified and handled anomalous values within the `sale_price` attribute using Box Plots, safeguarding the integrity and accuracy of the Average Order Value (AOV) and gross revenue metrics.

---
##  🛠️ Tech Stack & Methodology
* **Analysis Tools:** Google Colaboratory
* **Data Visualization:**
  * Matplotlib
  * Seaborn
  * Plotly
* **Algorithms:**
    * **Cohort Analysis:** Longitudinal study of retention rates.
    * **RFM Modelling:** Customer segmentation based on Recency, Frequency, and Monetary value.
    * **Apriori Algorithm:** Association rule mining for Market Basket Analysis.
    * **Pareto Analysis:** Identify the top 20% of inventory items that account for 80% of total revenue.
 
---

## 📈 Core Business Metrics (YTD)

| Metric | Value | Insights |
| :--- | :--- | :--- |
| **Total Revenue** | $10,796,335.70 | Shows a large revenue scale with steady growth. |
| **Net Profit** | $5,602,333.55 | Represents an outstanding Profit Margin of 51.89%. |
| **Average Order Value (AOV)** | $84.88 | Serves as the baseline for cross-selling strategies. |
| **Conversion Rate (CR)** | 18.51% | Abnormally high compared to the 2-3% industry benchmark, driven by aggressive acquisition of impulse buyers. |
| **Return Rate** | 9.97% | Results in a revenue leakage of approximately $1.07M. |

---

## 🔍 Strategic Deep Dive: Key Insights

### The Conversion Black Hole (Funnel & Sankey Analysis)
* **The Evidence:** Marketing drives high-quality traffic to product pages, but there is a uniform ~60% drop-off at the final stage: Cart -> Purchase. The total journey failure rate is 73.4%.
* **The Insight:** This is a Platform/UX failure, not a Marketing failure. Friction points are internal, such as hidden shipping fees, mandatory login walls, or payment gateway errors.
* **Impact:** Fixing just 10% of this bottleneck would recover over $1M in annual revenue without spending extra on Ads.

### The "One-Hit Wonder" Model & Leaky Bucket
* **The Evidence:** Multi-year cohort analysis shows retention plummets to 2%-5% by the second month. Furthermore, 13,000+ high-value customers are 'Hibernating' or 'Lost'.
* **The Insight:** The platform suffers from "Leaky Bucket Syndrome". The business is overly focused on "hunting" new users instead of "farming" loyal ones.
* **Impact:** A $1.33M potential resides in the dormant "Cannot Lose Them" segment, making a shift to retention vital.

### Revenue Pillars & Supply Chain Risks (Pareto Analysis)
* **The Evidence:** A Pareto (80/20) analysis reveals that 12 out of 26 categories generate 76% of total revenue.
* **The Insight:** The platform relies on a Seasonal Hedging strategy: Jeans are the "Cash Cow" providing non-seasonal steady cash flow, while Outerwear and Swimwear have perfectly inversely correlated seasonal peaks.
* **Risk:** High-revenue categories like Intimates and Jeans have high return volumes due to sizing sensitivities. Supplier-level quality control is the main driver of the ~41% overall order cancellation rate.

### Hidden Purchasing Patterns (Apriori Algorithm)
* **The Evidence:** Association Rule Mining identified high Lift scores for specific product pairs. For example, `[Lingerie] -> [Intimates]` shows the highest lift.
* **Opportunity:** Customers buying Denim are likely to purchase specific tops/accessories. Shifting to "Super Bundles" and automating a "Frequently Bought Together" engine could increase AOV from $84.88 to $100+.

---

## 🎯 Actionable Recommendations

### Priority 1: Plugging the "Leaky Bucket"
* **Optimize Checkout Friction:** Implement "Guest Checkout" to remove the mandatory account creation barrier and salvage the 60% final-step drop-off.
* **Transparent Cost Breakdown:** Display shipping fees and taxes early at the Cart stage to eliminate last-minute sticker shock.
* **Automate Abandoned Cart Recovery:** Deploy automated triggers at 1-hour and 24-hour intervals with a 5% discount or Free Shipping code.
* **Supply Chain Quality Audit:** Audit Intimates & Jeans suppliers exceeding a 50% defect threshold and enforce logistic penalty clauses.
* **Enhance Size & Fit Tools:** Integrate measurement-based Size Guides and "Customer Photo Reviews".

### Priority 2: Maximizing Revenue Per User
* **Recommendation Engine Integration:** Embed a "Frequently Bought Together" widget on Product and Checkout pages using Apriori algorithm outputs.
* **Strategic "Super Bundles":** Create pre-packaged product combinations (e.g., Jeans + Basic T-shirt) offered at a 7-10% bundle discount to push AOV beyond $84.88.

### Priority 3: Pivoting to Retention
* **Marketing Budget Re-allocation:** Divert 20-30% of the current acquisition ad budget towards Re-marketing (Win-back Campaigns) targeting the "At Risk" and "Cannot Lose Them" segments.
* **Launch a Tiered Loyalty Program:** Develop a points and tier-based reward system providing exclusive perks (e.g., lifetime free shipping for Gold members).
* **Intelligent Inventory Management:** Maintain a safety stock for Jeans to prevent out-of-stock scenarios, and synchronize the inventory cycles of Outerwear and Swimwear.

---

**Presenter:** Tien Phap  
**Project Completion Date:** 03/2026
