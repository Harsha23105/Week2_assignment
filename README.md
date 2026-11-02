# Week 2 - Data Modeling and Visualization Using Power BI

## Project Overview
This project focuses on data modeling and visualization using Microsoft Power BI. The Sample Superstore dataset is used to analyze sales performance across different regions and understand revenue trends over time.

## Objectives
- Import and clean the Superstore dataset.
- Create separate tables for Orders, Customers, Products, and Regions.
- Establish relationships between tables.
- Create a Calendar table using DAX.
- Build a Year-Month-Day date hierarchy.
- Create interactive sales visualizations.

## Tools Used
- Microsoft Power BI Desktop
- Power Query Editor
- DAX (Data Analysis Expressions)
- Kaggle Sample Superstore Dataset

## Dataset
The project uses the Sample Superstore dataset downloaded from Kaggle.

Important fields include:
- Order ID
- Order Date
- Customer ID
- Customer Name
- Product ID
- Product Name
- Category
- Region
- Sales
- Profit
- Quantity

## Data Preparation
1. Imported the Superstore CSV dataset into Power BI.
2. Cleaned and transformed the data using Power Query.
3. Created separate Customers, Products, and Regions tables using Reference queries.
4. Removed duplicate customer IDs, product IDs, and region values.
5. Checked and corrected the data types.

## Data Modeling
Created relationships between the following tables:

- Customers and Orders
- Products and Orders
- Regions and Orders
- Calendar and Orders

Established one-to-many relationships wherever applicable.

## Calendar Table
Created a Calendar table using DAX.

```dax
Calendar =
CALENDAR(
    MIN(Orders[Order Date]),
    MAX(Orders[Order Date])
)
```

Created the following calculated columns:
- Year
- Month
- Month Number
- Day

Created a Date Hierarchy with the following levels:

Year → Month → Day

## DAX Measure

Created a measure to calculate total sales.

```dax
Total Sales = SUM(Orders[Sales])
```

## Visualizations

### 1. Region-wise Sales Analysis
Created a bar chart to compare total sales across different regions.

### 2. Year Slicer
Created an interactive Year slicer to filter the report based on selected years.

### 3. Revenue Trends
Created a line chart to analyze sales trends over time using the Calendar Date Hierarchy.

## Key Learning Outcomes
- Understanding data modeling concepts.
- Creating table relationships in Power BI.
- Using Power Query for data transformation.
- Writing DAX formulas and measures.
- Creating date hierarchies.
- Designing interactive dashboards and visualizations.

## How to Run
1. Download the repository.
2. Open the Power BI `.pbix` file using Power BI Desktop.
3. Update the dataset path if required.
4. Refresh the data.
5. Explore the dashboard and interact with the Year slicer.

## Author
Harsha Lakshmi S

Computer Science and Engineering  
Artificial Intelligence and Machine Learning
