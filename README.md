# Retail Sales & Inventory Performance Analysis using SQL and Power BI 
(Retail Store Inventory and Sales Data project)
# Executive Summary
This project analyzes retail sales and inventory performance using SQL, Python, and Power BI.

The dataset contains detailed information on product categories, stock levels, pricing, and sales data from a retail store.

The goal was to identify trends in sales performance, analyze inventory turnover, and generate actionable insights for demand forecasting and stock optimization.
An interactive Power BI dashboard was created to visualize key metrics and support data-driven decisions.

Details of SQL as per this link
https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1sretail-project-475002!2sus-central1!3sd1d8b90a-53db-4386-9ff4-a1f2ab06dd56!2e1

Details of Python as per this link
https://colab.research.google.com/drive/1UAKHW73xEhtb32CRFyIQNya1W-5Z_4ND?usp=sharing

# Business Problem

Retail businesses often struggle with:
- Overstock and stockouts due to poor demand forecasting
- Limited visibility into product-level sales performance
- Lack of centralized dashboard to monitor real-time inventory status

The objective was to build a system that enables:
- Efficient tracking of stock and sales trends
- Identification of high-performing and underperforming products
- Insights to optimize inventory management
# Methodology
Step 1 — Data Extraction (SQL)
- Used SQL queries with CTEs, Joins, and CASE statements to extract and clean data from the retail sales database.
- Aggregated sales and inventory data by product category and store.

Step 2 — Data Processing (Python)
- Applied Pandas for cleaning and data transformation.
- Used Matplotlib and NumPy to explore trends and correlations.

Step 3 — Visualization (Power BI)
- Built an interactive Power BI dashboard with key KPIs:
  Sales Revenue
  Stock Level & Turnover Rate
  Top-Selling Categories
  Monthly Sales Trend
- Used DAX measures and data modeling to create relationships between tables.


# Skills
SQL: CTEs, Joins, Case, Aggregate functions

Power Bi:Dax, write functions, ETL, calculated columns, data visualization, data modeling

Python: Pandas, Matplotlib, Numpy, Writing functions, building a product funnel, statistics

# Results and Business Recommendations
1. Product Funnel Analysis
<img width="816" height="470" alt="image" src="https://github.com/user-attachments/assets/b3d8b29e-fca2-44e8-a271-3fd81ed85ebf" />

# Observation:
จากกราฟ “Product Funnel”
สินค้าที่ Fully Sold มีจำนวนคำสั่งซื้อสูงสุด (~38,000)
Partially Sold ประมาณ (~35,000)
ส่วน Ordered but not Sold มีน้อยมาก (<1,000)

# Interpretation:
ช่องทางการขายของร้านมีอัตราการขายสำเร็จสูงมาก (~95%) แสดงถึง ประสิทธิภาพของระบบ fulfillment และ demand forecasting ที่ดี
แต่สัดส่วน “Partially Sold” ที่ยังมีมาก (~47%) อาจบ่งชี้ถึงปัญหา สต็อกไม่เพียงพอ หรือการจัดการ order ที่ยังไม่สมบูรณ์

# Recommendation:
วิเคราะห์สาเหตุของ “Partially Sold” เพิ่มเติม เช่น ปัญหาสต็อก หรือสินค้าหมดกลางรอบโปรโมชั่น
พัฒนา inventory alert system เพื่อป้องกันสินค้าขาดช่วงระหว่าง order
สามารถใช้ Funnel นี้ติดตาม conversion rate ต่อเนื่อง และสร้าง KPI เพื่อ monitor “Order Fulfillment Rate”

2. Units Sold by Holiday / Promotion
<img width="540" height="393" alt="image" src="https://github.com/user-attachments/assets/5b8930ac-2b15-4ba2-a18e-bf6a63867551" />

# Observation:
จากกราฟพบว่า “ช่วงวันหยุด (Holiday)” มียอดขายสูงที่สุด (~220 units)
รองลงมาคือ “ช่วงมีโปรโมชั่น (Promotion)” (~150 units) และ “ไม่มีโปรโมชั่น/วันพิเศษ (None)” มียอดขายน้อยที่สุด (~80 units)

# Interpretation:
ช่วงวันหยุดและโปรโมชั่นมีอิทธิพลโดยตรงต่อยอดขาย เนื่องจากลูกค้ามีแนวโน้มจับจ่ายมากขึ้น
แต่การที่ “Holiday” ทำยอดขายสูงกว่า “Promotion” แสดงให้เห็นว่าพฤติกรรมการซื้ออาจได้รับผลจาก “เวลา” มากกว่า “ราคา”

# Recommendation:
ควรออกแคมเปญส่งเสริมการขาย ก่อนและระหว่างวันหยุดสำคัญ เพื่อเพิ่มยอดขายสูงสุด
ใช้ข้อมูลนี้ในการวางแผน inventory stocking และ workforce scheduling ให้เพียงพอช่วงเทศกาล


# Next Steps

1. Implement A/B testing for pricing and promotion strategies
2. Integrate real-time data feed from POS system into Power BI
3. Build a predictive model for demand forecasting using regression techniques
