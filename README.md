# olist-e-commerce-analytics
Product analytics case study of the Brazilian Olist e-commerce dataset (100k+ orders). Analyzed GMV dynamics, delivery delays impact, RFM segmentation, and category economics using SQL, Python, and Pandas.



#           Olist E-commerce Product Analytics Case Study

## Project Overview

This project presents an end-to-end product analytics study of Olist, the  e-commerce marketplace in Brazil (analyzing 100k+ orders from 2016 to 2018). 

  The goal of this project is to identify core business bottlenecks in customer retention, logistics performance, payment methods, and category economics to provide actionable recommendations for revenue growth and customer satisfaction.


##  Tech Stack & Methods

* **Data Storage & Querying:** PostgreSQL, DuckDB, SQL (JOINs, Aggregations, Window Functions, Subqueries)
* **Data Processing & Analysis:** Python, Pandas, NumPy
* **Data Visualization:** Plotly Express, Matplotlib, Seaborn
* **Environment:** Google Colab, Jupyter Notebook
* **Framework:** Fact → Root Cause / Business Impact → Recommendation



##  Key Analytical Highlights

* **Sales Driver:** GMV growth is almost entirely driven by order volume ($r = 0.990$), while Average Order Value (AOV) remains static.
* **Delivery vs Satisfaction:** On-time deliveries achieve a **4.29/5** score, whereas delayed orders drop to **2.57/5**.
* **Low Retention:** Over **97%** of customers buy only once, indicating a lack of post-purchase retention loops.
* **Regional Bottlenecks:** Delivery delays peak in **Bahia (14.0%)** and **Rio de Janeiro (13.5%)**, driving regional churn.
* **Shipping Friction:** Freight costs reach **50.6%** of item price in budget categories like Telephony, creating purchase barriers.


##  Core Insights & Executive Summary

### 1. Revenue Trends & Order Volume
* **Fact:** Monthly GMV strongly correlates with order volume ($r = 0.990$). Average Order Value (AOV) remains stable between $125 and $150.
* **Impact:** Revenue fluctuations are dictated by customer acquisition rather than changes in average spend per order.
* **Recommendation:** Focus marketing efforts on driving transaction volume and introduce cross-selling to increase basket size.

### 2. Delivery Delays & Customer Experience
* **Fact:** On-time deliveries achieve an average rating of **4.29 / 5**, while delayed orders drop sharply to **2.57 / 5**. Negative reviews (1–2 stars) surge from **6.64%** to **22.59%** when delivery exceeds 14 days.
* **Impact:** Logistics friction directly destroys user trust and drives bad reviews.
* **Recommendation:** Adjust estimated delivery dates (EDD) for remote regions and set up automated delay notifications to manage customer expectations.

### 3. Customer Retention & RFM Segmentation
* **Fact:** Over 97% of active users belong to single-purchase segments (`Sleeping`, `Lost`, or `Recent One-Timers`). Repeat purchase rates stay below **5%** regardless of the first order review score.
* **Impact:** High customer churn forces the business to continuously spend on acquiring new users (CAC).
* **Recommendation:** Build lifecycle email flows and post-purchase trigger discounts for `Recent One-Timers` within 30–60 days of their first order.

### 4. Regional Logistics Performance
* **Fact:** Delivery delays are geographically concentrated, peaking in **Bahia (14.0%)** and **Rio de Janeiro (13.5%)**, compared to ~5.9% in São Paulo.
* **Impact:** Long fulfillment times lead to regional user dissatisfaction in outer states.
* **Recommendation:** Partner with regional 3PL logistics hubs in BA and RJ to optimize last-mile delivery.

### 5. Category Economics & Payment Behavior
* **Fact:** Categories like `health_beauty` and `watches_gifts` lead total revenue, while `telephony` faces high freight friction with shipping costs reaching **50.6%** of the product price. Credit cards drive the highest average order value (~$160) with cancellation rates under 0.6%.
* **Impact:** High relative shipping costs decrease conversion rates on lower-priced accessories.
* **Recommendation:** Offer bundled shipping discounts on budget accessories to lower freight barriers.



## Project Structure
```text
├── olist_analytics.ipynb   # Main notebook (SQL queries, EDA & Visualizations)
└── README.md               # Executive Summary & Portfolio Documentation
