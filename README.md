# Retail Sales & Inventory Performance Analysis Project
# Executive Summary
This project analyzes retail sales and inventory data to identify sales trends, optimize stock levels and improve forecasting accuracy by using SQL, Python, and Power BI to extracted, cleaned and visualized to support data-driven decision-making.

A Power BI dashboard was created to visualize key metrics and support data-driven decisions.
https://drive.google.com/file/d/1pm55gCNfQzUek9UYT_-h9qtKU-qgdh1U/view?usp=sharing

Details of SQL as per this link
https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1sretail-project-475002!2sus-central1!3sd1d8b90a-53db-4386-9ff4-a1f2ab06dd56!2e1

Details of Python as per this link
https://colab.research.google.com/drive/1UAKHW73xEhtb32CRFyIQNya1W-5Z_4ND?usp=sharing

# Business Problem

Retail businesses often struggle with:
- Overstock and stockouts due to poor demand forecasting
- Limited visibility into real-time inventory performance
- Lack of centralized system for monitoring product sales

The goal are Build an end-to-end analytics pipeline to track performance, identify bottlenecks and provide actionable insights. 

# Methodology
Step 1 — Data Extraction (SQL)
- Used SQL queries with CTEs, Joins, and CASE statements to extract and clean data from the retail sales database.
- Aggregated sales and inventory data by product category and store.

Step 2 — Data Processing (Python)
- Applied Pandas for cleaning and data transformation.
- Used Matplotlib and NumPy to explore trends and correlations.

Step 3 — Visualization (Power BI)
- Built an interactive Power BI dashboard with key KPIs:
  Sales by category
  Inventory Turnover 
  Promotion vs Holiday sales
  Fullfillment rate

# Skills
SQL: CTEs, Joins, Case, Aggregate functions

Power Bi:Dax, write functions, ETL, calculated columns, data visualization, data modeling

Python: Pandas, Matplotlib, Numpy, Writing functions, building a product funnel, statistics

# Results and Business Recommendations
1. Product Funnel Analysis
<img width="816" height="470" alt="image" src="https://github.com/user-attachments/assets/b3d8b29e-fca2-44e8-a271-3fd81ed85ebf" />

# Observation:
- Fully Sold: products dominate (~38k orders)
- Partially Sold: ~35k orders -> nearly half of all sales
- Ordered but not Sola < 1k

# Interpretation:
High fulfillment efficiency (~95%) but 'Partially Sold' may indicate stock or order process issues.

# Recommendation:
- Investigate root causes of 'Partially Sold' items
- Add inventory alerts to prevent stockouts
- Create KPIs to monitor fulfillment rate

2. Units Sold by Holiday / Promotion
<img width="540" height="393" alt="image" src="https://github.com/user-attachments/assets/5b8930ac-2b15-4ba2-a18e-bf6a63867551" />

# Observation:
- Holiday Sales: highest (~220 units)
- Promotion : ~150 units
- No event : lowest (~80 units)

# Interpretation:
- High sales during Holidays suggest non-price factors (e.g., increased traffic/gift-giving) are primary drivers. Promotions are a secondary boost.

# Recommendation:
Test a strategy to launch promotions 1-2 weeks prior to holiday peaks to capture early spenders and maximize campaign reach.

3.  Category Performance and Seasonal Impact
   <img width="2808" height="1612" alt="image" src="https://github.com/user-attachments/assets/480e6941-9ca7-4032-9bd8-9145f38d1e48" />

# Observation:
Electronics and Toys drive ≈40% of total revenue. Groceries show the strongest seasonality, peaking in Winter (25.25% of annual sales).

# Interpretation:
The gap in Units Ordered vs Sold for Clothing (approx. 0.4M) suggests potential fulfillment bottlenecks, warranting immediate investigation.

# Recommendation:
Prioritize Winter stock allocation for Groceries. Investigate and resolve fulfillment/stock management issues for Clothing to optimize the sales pipeline.

# Next Steps
1. Implement A/B testing for pricing & campaign timimg
2. Integrate real-time POS data to Power BI
3. Develop predictive demand forcasting model



