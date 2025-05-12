![image](https://github.com/user-attachments/assets/fb10482a-04f7-41c6-be60-7870bc6e59cb)# Product Details Report
### Dashboard Link: https://app.powerbi.com/view?r=eyJrIjoiZGQ1MjQzODItNjQwMi00MWY3LTg0NGItYjdjYmExOTNmOTRhIiwidCI6ImE5ZTRjZmZlLWY5YzQtNGQ0MC04ZDE3LWY0M2I5OGJiM2YzZiJ9
##Problem Statement
This report provides a detailed overview of product sales across different countries, focusing on total units sold, revenue generated, and country-wise demand. It aims to help identify top-performing products and regional sales patterns for better inventory and marketing strategies.

### Steps Followed
Step 1: Loaded the sales data (Excel/CSV) into Power BI Desktop.

Step 2: Opened Power Query Editor and enabled:

Column Distribution

Column Quality

Column Profile

Step 3: Ensured data consistency and cleaned missing or incorrect values.

### Report Design & Visualization
Step 4: Applied a clean and readable Power BI theme for visual clarity.

Step 5: Added filters (slicers) for:

Country (Indian, Japan, Pairs, US)

Step 6: Used Card Visual to show:

Total Price: 867K

Step 7: Created a Table Visual showing:

Product Name

Total Units

Sum of Price

Country

Step 8: Designed a Bar Chart for:

Country-Wise Demand based on total units sold.

Step 9: Added a Column Chart for:

Top 5 Products by Total Sales:

Pencil: 271K

Books: 130K

Note: 108K

Scale: 85K

Label: 83K

### DAX Calculations
Step 10: Created key measures:

DAX
Copy
Edit
Total Units = SUM(Sales[Total unit])
Total Price = SUM(Sales[Sum of Price])
Step 11: Top Product Sales (used in visual filter or ranking):

DAX
Copy
Edit
Top Products = 
TOPN(5, SUMMARIZE(Sales, Sales[Product name], "TotalSales", SUM(Sales[Sum of Price])), [TotalSales], DESC)
Insights from the Report
## 1. Country-Wise Demand
Top Country by demand: Pairs (3584 units)

Followed by:

Japan: 3072 units

US: 2048 units

Indian: 1536 units

##2. Top Performing Products
Pencil is the best-selling product with 271K in sales.

Books, Note, Scale, and Label also perform well.

## Recommendations
Focus on Pairs and Japan for scaling product promotions.

Stock more of top-selling products like pencil and books to meet demand.

Investigate lower-performing regions for potential marketing or pricing strategy changes.

Use the insights for seasonal inventory planning and targeted offers.

### Snapshots of the Dashboard
Power BI Report View:
![image](https://github.com/user-attachments/assets/4a3c1f4b-9624-4e2c-a132-a33aa8b357d9)


### Conclusion
This report provides a high-level view of product sales by country and highlights key areas for business improvement. By leveraging Power BI visuals and DAX calculations, decision-makers can quickly identify opportunities and optimize product performance across regions.
