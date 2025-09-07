# Blinkit Sales Performance Analysis (Power BI)

## Project Overview
This project involves a comprehensive real-time Power BI dashboard for Blinkit, an online grocery shopping store by Zomato, to analyze its sales performance. The goal was to transform raw sales data from an Excel sheet into an interactive and dynamic dashboard, providing key insights into product performance, customer satisfaction, and outlet operations. This analysis helps in understanding business trends and supporting data-driven decision-making.

## Problem Statement & Business Requirements
The core objective was to conduct a comprehensive analysis of Blinkit's sales performance, customer satisfaction, and distribution effectiveness using Power BI. The project was guided by specific business requirements, to those provided by a client in a real-time scenario.

**Key Performance Indicator (KPI) Requirements:**  
The project required the calculation and visualization of the following high-level KPIs to provide an overall summary of the business performance:  
1. **Total Sales:** Overall revenue generated from all items sold.  
2. **Average Sales:** Average revenue per sale/order.  
3. **Number of Items:** Count of all items sold (each row in the dataset represents an item sold).  
4. **Average Rating:** Average customer rating for items sold, providing insight into customer satisfaction and product/service quality.

**Chart & Visualization Requirements:**  
To enable deep-dive analysis and departmental-level decision-making, several charts were required:  
1. **Total Sales by Fat Content (Donut Chart):** Analyze the impact of fat content on total sales, additionally visualized by average sales, number of items, and average ratings.  
2. **Total Sales by Item Type (Bar Chart):** Analyze sales performance across different item types (e.g snack foods, soft drinks, frozen foods), also visualized by average sales, number of items, and average ratings.  
3. **Fat Content by Outlet for Total Sales (Clustered Bar Chart):** Analyze fat content sales performance based on different outlet locations (Tier 1, Tier 2, Tier 3) and additional metrics.  
4. **Sales by Outlet Establishment (Line Chart):** Analyze total sales performance based on the year outlets were established, identifying top-performing outlets.  
5. **Sales by Outlet Size (Donut Chart):** Analyze sales based on outlet size (small, medium, high), identifying best-performing outlets by size.  
6. **Sales by Outlet Location (Funnel Chart):** Analyze sales performance based on outlet location tiers (Tier 1, Tier 2, Tier 3).  
7. **All Metrics by Outlet Type (Matrix Chart):** Visualize total sales, number of items, average sales, average ratings, and item visibility across different outlet types (e.g Supermarket 1, Grocery Store).

## Data Source & Description
The project utilized a single Excel file from kaggle [Blinkit Grocery Data on Kaggle](https://www.kaggle.com/datasets/arunkumaroraon/blinkit-grocery-dataset)

- **Rows:** Approximately 8,500 rows (8,523 after header removal)  
- **Columns:** 12 fields  

**Key Fields:**  
- **Item Fat Content:** Categorizes products by fat content (e.g Low Fat, Regular)  
- **Item Identifier:** Unique code for each product  
- **Item Type:** Categories of products (e.g Snack Foods, Soft Drinks, Fruits and Vegetables)  
- **Outlet Establishment Year:** Year the outlet was established  
- **Outlet Identifier:** Unique code for each outlet  
- **Outlet Location Type:** Tier classification of the city where the outlet is located (Tier 1, Tier 2, Tier 3)  
- **Outlet Size:** Size classification of the outlet (Small, Medium, High)  
- **Outlet Type:** Type of outlet (e.g Supermarket 1, Grocery Store)  
- **Item Visibility:** How visible an item is in the online app  
- **Item Weight:** Weight of the item  
- **Sales:** Total sales for a particular order/item  
- **Rating:** Customer rating for the purchased item/service  

## Tools Used
- **Microsoft Power BI Desktop:** Data connection, transformation, modeling, DAX calculations, visualization, dashboard creation  
- **Power Query Editor:** Embedded within Power BI for data cleaning and transformation  

## Methodology / Steps Taken
The project followed a structured approach to ensure an insightful dashboard:  

1. **Requirement Gathering:** Defined all business needs, including specific KPIs and charts  
2. **Data Walkthrough:** Examined the raw Excel data to understand its structure and content  
3. **Data Connection:** Connected Power BI Desktop to the Excel data source  
4. **Data Quality Check & Cleaning:**  
   - Standardized **Item Fat Content** values (e.g 'LF' → 'Low Fat', 'R' → 'Regular', 'low fat' → 'Low Fat')  
   - Checked column quality for validity, errors, and empty values  
   - Noted some numerical fields (like Item Weight) had missing values (16%), acceptable for this analysis  
5. **Data Processing & Modeling:** Ensured correct data types and relationships  
6. **DAX Calculations:** Created KPI measures:  
   - **Total Sales = SUM(Blinkit Grocery Data[Sales])**  
   - **Average Sales = AVERAGE(Blinkit Grocery Data[Sales])**  
   - **Number of Items = COUNTROWS('Blinkit Grocery Data')**  
   - **Average Rating = AVERAGE(Blinkit Grocery Data[Rating])**  
7. **Dashboard Layout & Formatting:**  
   - Custom canvas size (800x1400 px) with 40% transparency  
   - Left-hand navigation panel styled with Blinkit brand colors  
   - Added dashboard title "Blinkit" 
8. **Chart Development & Formatting:**  
   - Field Parameters to dynamically switch between Total Sales, Average Sales, Number of Items, and Average Ratings  
   - Interactive slicers for Outlet Location, Outlet Size, and Item Type  
   - Configured cross-filter interactions  
   - Added "Clear All Filters" button  
9. **Report / Dashboard Generation:** Integrated all elements into a cohesive dashboard  
10. **Insight Generation:** Analyzed visualizations to extract actionable insights  

## Key Results & Insights
The final interactive dashboard provides a **comprehensive view of Blinkit's sales performance**:

1. **Key Performance Indicators (KPIs):**  
   - **Total Sales:** $1.2 million  
   - **Average Sales:** $141 per order  
   - **Number of Items:** 8,523 items sold  
   - **Average Rating:** 3.9 out of 5  

2. **Product-Level Insights:**  
   - **Total Sales by Fat Content:** 65% of orders are 'Low Fat' products  
   - **Total Sales by Item Type:** "Fruits and Vegetables" are the best-selling items  
   - **Fat Content by Outlet:** Tier 3 cities have the largest sales, with 'Low Fat' items dominating  

3. **Outlet-Level Insights:**  
   - **Total Sales by Outlet Establishment:** Outlets established in 2018 are highest performing  
   - **Sales by Outlet Size:** "Medium" outlets generated the highest sales  
   - **Sales by Outlet Location:** Tier 3 cities contribute the most to total sales  
   - **All Metrics by Outlet Type:** Matrix chart shows performance differences between Supermarket 1 and Grocery Stores  

4. **Interactive Filtering:**  
   - Slicers for Outlet Location, Outlet Size, and Item Type  
   - "Clear All Filters" button for quick reset  

## Technical Skills Demonstrated
- **Data Connection & Loading:** Excel -> Power BI  
- **Data Cleaning & Transformation:** Power Query Editor standardization  
- **DAX (Data Analysis Expressions):** Custom KPI measures  
- **Data Modeling:** Relationships and data types management  
- **Interactive Dashboard Design:** Slicers and cross-filtering  
- **Field Parameters:** Dynamic metric switching in charts  
- **Advanced Visualization:** Donut, Bar, Clustered Bar, Line, Funnel, Matrix  
- **Dashboard Formatting & Layout:** Brand-aligned colors, canvas customization  

## Future Enhancements
- Explore time-series analysis on item types  
- Segment customers based on purchasing behavior  
- Add predictive analytics for sales forecasting  
- Create an interactive online version for executive reporting  
