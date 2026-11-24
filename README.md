# CognoRise Info Tech Internship Projects

A collection of three end-to-end data analytics projects completed as part of my **CognoRise InfoTech** data analytics internship. Each project goes from raw data to a finished, interactive **Power BI dashboard** with insights, recommendations and data limitations.

| # | Project | Level | Tools | Dataset |
|---|---------|-------|-------|---------|
| 1 | [Retail Sales Analysis](#project-1--retail-sales-analysis) | Beginner | Power BI | Kaggle: Retail Sales Dataset |
| 2 | [E-Commerce Customer & Sales Analytics](#project-2--e-commerce-customer--sales-analytics) | Intermediate | MySQL, Power BI | Kaggle: E-Commerce Dataset |
| 3 | [Marketing Campaign Performance](#project-3--marketing-campaign-performance) | Advanced | SQL, Power BI | Kaggle: Marketing Campaign Performance Dataset |

---

## Project 1 — Retail Sales Analysis

**Level:** Beginner | **Tools:** Excel,Power BI | **Dataset:** Kaggle Retail Sales Dataset

### Objective
Clean and validate transaction data, calculate core sales KPIs, analyze sales by category, month and customer segment, and recommend ways to improve sales performance.

### Dashboard Pages
- **Overview**: KPI cards, sales trend by month, category-wise sales, sales by gender and age, date and product category slicers
- **Insights & Recommendations**: key insights, recommendations and limitations

### Key KPIs
| Metric | Value |
|--------|-------|
| Total Revenue | 456K |
| Total Transactions | 1,000 |
| Total Quantity Sold | ~3K |
| Average Order Value | 456 |
| Total Customers | 1,000 |

### Key Insights
- **Categories are close:** Electronics leads (156.9K), Clothing is close behind (155.6K), Beauty is lowest (143.5K). The gap between top and bottom is only about 8%.
- **Seasonality:** May is the peak month (53.2K), September the lowest (23.6K). Q4 is the strongest quarter (126.2K) and Q3 the weakest (96.0K).
- **Customers:** Female customers spend slightly more (232.8K vs 223.2K). Ages 18–25 have the highest average order (500).
- **Price tiers:** Products priced at 300 and 500 bring in 88% of revenue from only 40% of transactions.
- **Peak day:** Saturday has the highest sales and Thursday the lowest.

### Recommendations
1. Focus on high-value items: promote and bundle the 300 and 500 price-point products.
2. Smooth out seasonal dips with campaigns in September and March, and prepare stock and staffing for May and October.
3. Lift Beauty with targeted offers, especially for male customers.
4. Target by age: premium products for 18–25, volume deals for 46–55.
5. Schedule promotions around Saturday and add a midweek offer to lift Thursday.

### Limitations
No cost data (profit could not be calculated), no region or product-name fields, only one year of data, each customer appears once, and the small sample (1,000 transactions) appears to be practice data, so findings are indicative only.

---

## Project 2 — E-Commerce Customer & Sales Analytics

**Level:** Intermediate | **Tools:** MySQL Workbench, Power BI | **Dataset:** Kaggle E-Commerce Dataset (~1 million rows)

### Objective
Use SQL to extract and transform product, customer and sales data, analyze revenue and profit drivers, find high-revenue but low-profit products, and build a Power BI dashboard from the SQL analytical dataset.

### Approach
1. Imported ~1,000,000 rows from a Kaggle CSV into MySQL (`diversified_ecommerce`).
2. Transformed and aggregated the data with SQL.
3. Loaded the result into Power BI and built a 3-page dashboard.

### Dashboard Pages
- **Overview**: KPI cards, revenue by category, location and seasonality, slicers (product, age group, category)
- **Profit Analysis**: loss records and loss % by price band, category margin table, insights
- **Product Analysis**: revenue vs margin by product, top 10 products by loss %, recommendations

### Key KPIs
| Metric | Value |
|--------|-------|
| Total Revenue | 879.30M |
| Records | 1M |
| Distinct Products | 9K (43 product types) |
| Avg Margin | 762.07 |
| Avg Return Rate | 10.49% |
| Loss Rate | 1.16% |

### Key Insights
- **Balanced business:** All five categories earn 175M–177M, all 15 cities earn 57.9M–59.0M, and seasonality splits revenue about 50/50, so no category, location or product needs its own strategy.
- **Losses are rare:** Only about 1.16% of records (~11.6K of 1M) have a negative estimated margin.
- **Price is the driver of losses:** Every loss-making record is priced under 100. In the Under 50 band, 52.9% of records lose money; items priced 100 and above never do.
- **Shipping turns cheap items into losses:** Loss-making records average about 36 in shipping vs about 25 overall.
- **Premium items carry the business:** The 500+ price band is 75% of records and 94% of revenue (824M of 879M) with no losses.
- **Product level:** Loss % stays close to average across products (highest: Hiking Shoes, 1.31%).

### Recommendations
1. Set a minimum price or shipping threshold for items under 50.
2. Protect the 500+ band: keep it central in promotions and stock.
3. Don't run separate strategies by category, location or product; focus on price and shipping.
4. Check New York, which has the lowest margin (755.31).
5. Collect better data (order IDs, customer IDs, dates, product costs) to enable repeat-customer, time-trend and true profit analysis.

### Limitations
Profit is **estimated** (net price after returns minus shipping). The dataset has no orders, customers, dates or costs, so repeat-customer and time-trend analysis were not possible.

---

## Project 3 — Marketing Campaign Performance

**Level:** Advanced | **Tools:** SQL, Power BI | **Dataset:** Kaggle Marketing Campaign Performance Dataset

### Objective
Clean and combine campaign data across channels, calculate impressions, clicks, CTR, conversions, spend, CPC, CPA and ROI/ROAS, compare performance by campaign, channel, audience and time, and recommend where marketing spend should be increased, reduced or optimized.

### Approach
1. Cleaned and analyzed the data in SQL, creating analytical tables (campaign, channel, audience, date, duration and company cost/conversion analysis).
2. Imported the tables into Power BI.
3. Built a 6-page interactive dashboard with page navigation.

### Dashboard Pages
- **Executive Summary**: headline KPIs, performance over time, channel-wise and campaign-type performance, location filter
- **Campaign Analysis**: ROI, campaign count, acquisition cost, clicks, engagement, CPA and CPC by campaign type
- **Channel Analysis**: Email, Website, Google Ads, YouTube, Instagram and Facebook compared on conversion rate, ROI, engagement and cost
- **Time Analysis**: campaigns by month, plus cost, ROI, clicks, engagement and conversion rate by quarter
- **Audience Analysis**: Men 18–24, Men 25–34, Women 25–34, Women 35–44 and All Ages
- **Insights & Recommendations**: spend vs conversions, CPA by channel and campaign type, insights and recommendations

### Key KPIs
| Metric | Value |
|--------|-------|
| Total Campaigns | 200K |
| Total Spend | 2.50bn |
| Total Clicks | 110M |
| Total Impressions | 1bn |
| Total Conversions | ~8.80M |
| CPA | 284.04 |
| Average ROI / ROAS | ~5.0 |

### Key Insights
- **No segment stands out:** Channel, campaign type, audience, location, duration and quarter all sit within ±1% of the average CPA, and tests show no significant differences.
- **Spend doesn't drive conversions:** The correlation between spend and conversions is about 0.00, and every cost band gets about 44 conversions per campaign. As a result, CPA rises from $148 (cheapest campaigns) to $421 (most expensive).
- **Time is flat:** Daily spend is steady and ROI is about 5.0 throughout the year.

### Recommendations
- **Reduce** cost on high-cost campaigns ($17K–$20K). Bringing them to the average cost at the same conversions would save about $240M (~10%); this is an illustrative estimate.
- **Optimize** by setting a per-campaign cost cap and testing creative and targeting, since nothing in the data explains performance.
- **Hold** the current channel, audience and campaign-type mix, and test any shift before committing.

---

## Skills Demonstrated
- Data cleaning and validation
- SQL (extraction, transformation, aggregation, analytical tables)
- KPI design and measures in Power BI
- Interactive dashboard design (multi-page, slicers, navigation)
- Business insight writing and recommendations
- Acknowledging data limitations honestly

## Repository Structure
```
.
├── README.md
├── project-1-retail-sales/
├── project-2-ecommerce-analytics/
├── project-3-marketing-campaign/
```


## About
Completed during the **CognoRise InfoTech** data analytics internship.

**Author:** Rinsha Fathima PC · [LinkedIn](https://linkedin.com/in/rinsha-fathima-pc-a85518388) · [Email](rinshafathimaapc@gmail.com)

