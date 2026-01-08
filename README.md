OLIST E-COMMERCE ANALYSIS
## Project Overview

This project provides a data-driven deep dive into the operational performance of **Olist**, Brazil's largest department store marketplace. I analyzed over 100k orders to quantify how shipping speed directly impacts customer satisfaction and brand loyalty.

### The Business Challenge

The platform faced a critical operational hurdle: **over 54% of orders were delivered late.** My objective was to find the "Sentiment Cliff"—the exact point where delivery delays turn a 5-star experience into a 1-star review.

---

## Data Engineering & The "Master Table" Solution

### Solving the "Flat Line" Error

During the initial build, a relationship bottleneck between the `Orders` and `Reviews` tables caused all charts to show a stagnant 4.1-star average (a "flat line").

* **The Fix:** I engineered a **Master Fact Table** by merging datasets in Power Query. This bypassed the "filter bridge" issue, ensuring that my delivery tiers could accurately slice the review data.

### Logistics Segmentation (Delivery Tiers)

I categorized all deliveries into three distinct performance buckets:

* ** Rapid Tier (0-5 Days):** The "Delight" window.
* ** Standard Tier (6-10 Days):** The baseline market expectation.
* ** Late Tier (11+ Days):** The high-risk friction zone.

---

## Core Analysis: Speed vs. Sentiment

### 1. The Sentiment Cliff

By mapping the three tiers against average review scores, I discovered that **Rapid** deliveries maintain a **~4.7-star average**, while **Late** deliveries drop significantly to **~3.3 stars**.

### 2. Correlation Analysis

The data confirms a strong negative correlation: as delivery days increase, the review score follows a downward slope. This proves that logistics speed is the #1 predictor of customer satisfaction for Olist.

### 3. High-Friction Product Categories

Identifying categories that "suffer the most" from delays:

* **Office Furniture:** Highly sensitive to the Late Tier due to shipping damage and assembly expectations.
* **Fixed Telephony:** High-tech products that result in 1-star reviews when not delivered on time.

---

## Strategic KPIs

| KPI | Value | Business Significance |
| --- | --- | --- |
| **Delight Rate** | **~58%** | Percentage of 5-star reviews (driven by the Rapid Tier). |
| **ARPU** | **$160.58** | Average Revenue Per User—identifying high-value customers. |
| **Retention Rate** | **6.07%** | A critical insight showing that 93.9% of users are one-time buyers. |
| **Avg Freight** | **$20.00** | The average hidden cost of shipping across the platform. |

---

## Strategic Recommendations

1. **The "Pre-emptive Discount":** Automatically send a loyalty voucher to any customer whose order enters the **Late Tier** *before* they leave a review to mitigate 1-star ratings.
2. **Category Specific Audit:** Focus on improving the shipping infrastructure for **Furniture** and **Auto Parts**, which show the highest dissatisfaction when delayed.
3. **Loyalty Program:** With a 93% one-time buyer rate, Olist should use the high satisfaction of the **Rapid Tier** to launch a subscription-based "Prime" service.
