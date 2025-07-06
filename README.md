📊 Power BI Sales Dashboard

This project showcases a complete Power BI data analytics workflow, starting from raw data normalization to a dynamic, interactive sales dashboard. The dashboard highlights customer demographics, product category performance, sales by geography, and overall KPIs.

✅ Features

🔄 Normalized data model (Star Schema)


🔗 Defined relationships between Fact and Dimension tables


🧮 DAX measures created:


TotalSales


CustomerCount


TotalProducts


📊 Interactive visuals:


Sales by Age Group, Gender, Occupation, Product Category, and State


KPI Cards for key metrics


Dynamic donut charts


📁 Data Model Structure

🧱 Tables:

FactSales (User_ID, Product_ID, Amount, etc.)

DimUsers (User_ID, Cust_Name, Gender, Age_Group, State, etc.)

DimProduct (Product_ID, Product_Category)

DimAddress (State, Zone)

🔗 Relationships:
FactSales[User_ID] → DimUsers[User_ID]

FactSales[Product_ID] → DimProduct[Product_ID]

DimUsers[State] → DimAddress[State]

🧠 Key Measures
DAX
Copy
Edit
TotalSales = SUM(FactSales[Amount])
CustomerCount = DISTINCTCOUNT(DimUsers[User_ID])
TotalProducts = DISTINCTCOUNT(FactSales[Product_ID])
📊 Visuals in the Report
Visual Title	Type	Purpose
TotalSales by Age Group	Funnel Chart	See which age group drives revenue
TotalSales by Product Category	Bar Chart	Top-selling product types
Sales by State	Column Chart	Geographic distribution
TotalSales by Gender	Donut Chart	Gender-based sales distribution
Sales by Occupation	Line/Area Chart	Customer profession insights
KPI Cards	Cards	Key business metrics summary

🧱 Tools Used
Power BI Desktop

DAX (Data Analysis Expressions)

Power Query (M Language)

Star Schema Modeling

📌 How to Use
Open the .pbix file in Power BI Desktop

Connect or refresh the dataset

Interact with slicers and visuals to analyze sales insights

✨ Screenshot
![Screenshot 2025-07-06 160614](https://github.com/user-attachments/assets/d885cb4a-6d66-4d2a-a566-47dc84a202b6)


💡 Author Notes
This project demonstrates best practices in Power BI including data normalization, relationship modeling, dynamic measures, and interactive reporting.
