# Sales Dashboard

A comprehensive sales dashboard providing insights into sales performance, helping businesses understand trends, identify key drivers, and make informed decisions.

### Dashboard Link: [Sales Dashboard](https://app.powerbi.com/groups/me/reports/afc10a13-1aa2-4cfc-89e6-4391b9591ca9/6c3a15e0e65d00c2269b?experience=power-bi)

## Problem Statement

This dashboard helps businesses understand their sales performance over the past three years. By analyzing various metrics, it provides insights into trends, key drivers, and areas for improvement. The dashboard also helps identify top-performing products, regions, and sales representatives, enabling businesses to strategize effectively.

### Steps Followed

- **Step 1**: Load data into Power BI Desktop from multiple sources, including Excel spreadsheets and databases.
- **Step 2**: Open Power Query Editor and check "column distribution," "column quality," and "column profile" options.
- **Step 3**: Ensure column profiling is based on the entire dataset.
- **Step 4**: Handle missing values appropriately. For example, null values in certain columns were excluded from calculations where necessary.
- **Step 5**: Choose a theme for the report view for a consistent look and feel.
- **Step 6**: Add new visuals using the visualizations pane for different metrics such as total sales, average sales, and sales growth.
- **Step 7**: Add slicers for fields such as product category, region, and sales representative for dynamic filtering.
- **Step 8**: Create card visuals to display key metrics like total sales, average sales, and sales growth.
- **Step 9**: Add bar charts to represent the number of sales by product category, region, and sales representative.
- **Step 10**: Create calculated columns and measures using DAX expressions to enhance the analysis.

### Key Calculated Columns and Measures

- **Sales Performance**: Grouping sales performance into various categories using the following DAX expression:
  ```DAX
  Sales Performance = 
  IF(SalesData[SalesAmount] > 100000, "High",
  IF(SalesData[SalesAmount] > 50000, "Medium", "Low"))

Count of Customers = COUNT(SalesData[CustomerID])

% Customers = (DIVIDE([Count of Customers], CALCULATE(COUNT(SalesData[CustomerID]), ALL(SalesData))) * 100)

Total Sales = SUM(SalesData[SalesAmount])

Average Sales = AVERAGE(SalesData[SalesAmount])

Sales Growth = (DIVIDE([Total Sales], [Previous Period Sales]) - 1) * 100


# Visual Filters (Slicers)
Product Category: Filter by different product categories.
Region: Filter by geographic regions.
Sales Representative: Filter by sales representatives.
Customer Segment: Filter by customer segments.

### Insights
**1** Total Number of Customers,      
**2** Total Customers: 10,000       
**3** Number of Repeat Customers: 6,000 (60%)         
**4** Number of New Customers: 4,000 (40%)
**5** Average Sales  
**6** Average Sales per Transaction: $150  
**7** Sales Growth  
**8** Sales Growth over the last year: 8%
### Top Performing Regions
-North America: $500,000   
-Europe: $400,000  
-Asia: $300,000 
### Customer Segment Distribution
-Retail: 70%  
-Wholesale: 30%  
### Age Group Distribution
-18-25: 15%  
-26-35: 45%  
-36-45: 25%  
-46-60: 10%  
-60+: 5%
### Customer Type
-Returning: 60%  
-New: 40%  
### Type of Purchase
-Online: 55%  
-In-Store: 45%  
-Publishing  
-The report was published to Power BI Service for broader access and collaboration.

### Conclusion
This sales dashboard provides a detailed overview of sales performance, helping businesses make data-driven decisions. By identifying key trends and areas for improvement, businesses can optimize their strategies and enhance their overall performance.
