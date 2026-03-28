# Marketing Funnel & Conversion Performance Analysis

> **End-to-end funnel analysis** exploring how 10,000 e-commerce users move through Browse → Add to Cart → Checkout → Purchase — uncovering drop-off points, channel performance, and revenue drivers using Python.


---

##  Project Overview

This project was completed as a **Final Task for Future Interns — Marketing Analytics Track**. The goal was to perform a full marketing funnel analysis on an e-commerce event dataset to understand user behaviour at each stage of the purchase journey.

Funnel analysis is core work in **startups, digital marketing agencies, SaaS companies, and sales teams** because improving conversion rates at any stage directly increases revenue — often without acquiring a single new customer.

The analysis covers:

- **Funnel stage conversion rates** at each step (Browse → Cart → Checkout → Purchase)
- **Drop-off quantification** — where and how many users are lost
- **Channel performance** — which marketing channels drive the most conversions
- **Device & region breakdowns** — how platform and geography affect conversions
- **Product category analysis** — which categories generate the most revenue and convert best
- **Time-based trends** — daily revenue patterns and a purchase heatmap by day/hour
- **Revenue KPIs** — total revenue, average order value, and revenue distribution
- **Actionable recommendations** — data-backed suggestions to improve each stage

---

##  Business Questions Answered

| # | Question | 
|---|----------|
| 1 | What is the overall conversion rate from visitor to customer? 
| 2 | Where are users dropping off the most in the funnel? 
| 3 | Which marketing channels bring the highest-quality leads? 
| 4 | Does device type affect conversion rates? 
| 5 | Which product categories drive the most revenue?
| 6 | When are users most likely to make a purchase? 
| 7 | What is the average order value and revenue distribution? 
| 8 | How can conversion rates be improved at each stage? 
---

## Dataset Description

**File:** `Funnel_Analysis_Data.csv`  
**Rows:** ~21,000 events  
**Users:** 10,000 unique users  
**Date Range:** December 2025 – January 2026

| Column | Type | Description |
|--------|------|-------------|
| `User ID` | String | Unique user identifier (e.g. USR-00001) |
| `Session ID` | String | Unique session identifier |
| `Event Time` | Datetime | Timestamp of the event |
| `Event` | String | Funnel stage: Browse, Add to Cart, Checkout, Purchase |
| `Device` | String | Device used: Mobile, Desktop, Tablet |
| `Region` | String | Geographic region: North, South, East, West |
| `Channel` | String | Marketing channel: Organic, Email, Google Ads, Social Media |
| `Product Category` | String | Category: Electronics, Fashion, Beauty, Sports, Home |
| `Revenue` | Float | Revenue generated (0.0 for non-purchase events) |
| `Bonus Flag` | String | Promotional flag (Yes/No) |

**Funnel Structure:**
```
Browse  →  Add to Cart  →  Checkout  →  Purchase
  (1)           (2)            (3)          (4)
```



##  Key Findings

> *Exact values are computed dynamically by the notebook from the dataset. Below are the types of insights surfaced.*

### Funnel Conversion Summary
```
Browse          → 10,000 users  (100.0%)
Add to Cart     →  6,949 users  ( 69.5%)   ← Step CR: 69.5%  | Lost 3,051 users
Checkout        →  3,456 users  ( 34.6%)   ← Step CR: 49.7%  | Lost 3,493 users  Biggest drop
Purchase        →  1,004 users  ( 10.0%)   ← Step CR: 29.1%  | Lost 2,452 users
```
**Overall conversion rate (Browse → Purchase): 10.0%**
```

###  Channel Performance
- Channels vary significantly in conversion rate — the best-performing channel converts at more than double the rate of the worst
- Not every high-traffic channel produces the best conversions — this has direct budget implications

###  Device Insights
- Desktop users tend to convert at a higher rate than mobile users
- Mobile represents the largest share of traffic but may have UX friction reducing conversions

###  Product Categories
- Revenue is unevenly distributed across categories — a small number of categories drive the majority of total revenue
- Some categories show high conversion rates but low average order value, and vice versa

###  Time Patterns
- Purchases cluster around specific hours and days of the week
- Certain weekday + time combinations consistently outperform others

---


##  Technologies Used

| Tool | 
|------|
| **Python** | 
| **Pandas** | 
| **NumPy** |
| **Matplotlib** | 
| **Seaborn** |
| **Jupyter Notebook** | 

---

##  Recommendations

Based on the analysis, the following strategies are recommended to improve funnel performance:

1. **Reduce Browse → Cart Drop-Off** — Improve product page CTAs, add social proof (reviews, ratings), and use personalised recommendations.

2. **Recover Abandoned Carts** — Implement cart-abandonment email sequences within 1 hour. Offer limited-time discount codes to incentivise users to return.

3. **Streamline the Checkout Process** — Reduce form fields, offer guest checkout, and display trust signals (SSL badge, free returns policy) prominently.

4. **Invest in Top-Performing Channels** — Reallocate marketing budget to the highest-converting channels; pause or restructure underperforming ones.

5. **Optimise for the Best-Converting Device** — Conduct UX audits on under-performing device types. Prioritise mobile checkout speed and simplicity.

6. **Promote High-Revenue Categories** — Feature top-revenue product categories in landing pages and ad campaigns. Cross-sell complementary products at checkout.

7. **Time-Based Promotions** — Use the purchase heatmap to schedule flash sales and push notifications during peak buying hours and days.

---

