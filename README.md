# Adidas-Sales-PBI
## Table of Contents

1. [Adidas in 2020-2021](#adidas-in-2020-2021)
2. [Objective](#objective)
3. [Data Source and Collection](#data-source-and-collection)
4. [Data Optimization and Transformation](#data-optimization-and-transformation)
5. [Database Management Systems](#database-management-systems)
6. [Integration with Power BI](#integration-with-power-bi)
7. [Visualizations in Power BI](#visualizations-in-power-bi)
8. [Key Questions and Analysis](#key-questions-and-analysis)
9. [Conclusion](#conclusion)
10. [References](#references)

---

## Adidas in 2020-2021
Adidas faced significant challenges due to the COVID-19 pandemic in 2020, including store closures, supply chain disruptions, and shifts in consumer behavior. Sales declined sharply during March and April 2020, varying across regions. By 2021, as vaccination campaigns advanced and economies reopened, sales steadily recovered. E-commerce emerged as a key growth driver, highlighting the brand's resilience and adaptability.

## Objective
The objective was to design and develop a Data Warehouse using MySQL and analyze Adidas' sales data from the provided dataset, "BD Adidas US Sales," through Power BI visualizations and dashboards.

## Data Source and Collection
- **Dataset Format**: Excel file
- **Content**: U.S. sales data, including retailer names, sales channels, geographies, product categories, and financial performance metrics.
- **Size**: 13 columns, 9648 rows

### Key Fields
- Retailer names and IDs
- Sales geographies (regions, states, cities)
- Product categories
- Financial data (price, units sold, total sales, operating profit, margins)

## Data Optimization and Transformation
- Data cleaning and preparation in Excel:
  - Removal of dollar signs (`$`) and percentage symbols (`%`).
  - Conversion of `Operating Margin` to decimal format.
  - Validation and correction of calculated fields like `Total Sales`.
- Data divided into nine CSV files for seamless MySQL import.

## Database Management Systems
### MySQL
- Schema creation: `adidas_db`
  ![image](https://github.com/user-attachments/assets/54ca2fcb-cd69-4be2-88c8-1d9d390534c2)

- Tables: Fact tables and dimension tables following star schema principles.
- Data relationships established with primary and foreign keys.
- ![image](https://github.com/user-attachments/assets/01f24e51-d554-4fb5-a6f7-14b0d1b51efe)


### Key Features
- Reverse engineering in MySQL Workbench to visualize schema.
  ![image](https://github.com/user-attachments/assets/ab1f740d-e165-4d60-b412-355d0c47e604)

- Use of SQL scripts for data transformation.

## Integration with Power BI
### Workflow
1. MySQL to Power BI data connection using MySQL Connector/ODBC Driver.
2. Data import and transformation in Power BI.
3. Creation of dimension and fact tables (e.g., `DimCalendario`, `FactsSales`).
![image](https://github.com/user-attachments/assets/75063f87-e7b3-4f14-b113-814acc2be852)

4. Development of a snow flake schema for optimized reporting.
![image](https://github.com/user-attachments/assets/09a2f36a-2ea6-4ba8-b16f-465d82145e83)

### Model Design
- **Fact Table**: Consolidates metrics like Total Sales, Operating Profit, Units Sold.
- **Dimension Tables**: Include product, geography, time, and sales channels.

## Visualizations in Power BI
### Dashboard Highlights
- **Sales Overview**: Total Sales (€120M), Operating Margin (€47M), Units Sold (2M), and more.
![image](https://github.com/user-attachments/assets/3d71d286-5695-486a-8814-55fe1dbfd4cf)

- **Trend Analysis**: Monthly trends of sales and profit by regions and retailers.
![image](https://github.com/user-attachments/assets/340e8d41-63ac-4b47-a94e-842ff53baf04)

- **Product Analysis**: Revenue and profit segmentation by product categories and channels.
![image](https://github.com/user-attachments/assets/68b1412e-60b6-4d4c-9a0f-30f8c3aa5a26)


### Interactive Features
- Buttons for navigation between report sections.
- Filters for detailed analysis by region, retailer, and sales method.

## Key Questions and Analysis
### 1. Regions, States, and Cities with Highest Sales
- **Regions**: West (€33M), Northeast (€32M).
- **States**: California (€18M), New York (€16M).
- **Cities**: New York (€5.7M), San Francisco (€4.9M).

### 2. Top Product Categories
- Women's Apparel (€22M), Women's Street Footwear (€21M), Men's Street Footwear (€20M).

### 3. Retailer Performance
- **Top Performer**: West Gear (€32M sales, €12M profit).
- **Highest Margin**: Sports Direct (44%).

### 4. Sales by Channel
- **Online**: €45M (44% margin).
- **Outlet**: €40M (38% margin).
- **In-Store**: €36M (36% margin).

### 5. Operational Profit and Margins
- Top regions: Northeast (40%+ margins).
- Categories: Men's and Women's Footwear dominate profitability.

## Conclusion
Adidas demonstrated resilience during 2020-2021 by leveraging digital channels and product innovation. The e-commerce channel emerged as the most profitable, supported by efficient operations and customer-centric strategies. Geographical and product performance insights highlight areas for growth and optimization.

## References
1. Adidas Group (2021). Retrieved from [Adidas 2021 Report](https://report.adidas-group.com/2021/en/group-management-report-our-company/global-sales.html)
2. Bautista, R. (2023). Case Study on Adidas Monthly Sales Analysis. [LinkedIn](https://www.linkedin.com/pulse/case-study-adidas-monthly-sales-analysis-2020-2021-renz-bautista/)
3. Datageeks (2024). [Data Warehouse Overview](https://www.datageeks.com.br/data-warehouse/)
4. Europeia (2024). [Power BI Overview](https://www.europeia.pt/blog/o-que-e-o-power-bi/)
5. Geeksforgeeks (2024). [MySQL Overview](https://www.geeksforgeeks.org/what-is-mysql/)
