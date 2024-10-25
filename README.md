**AdventureWorksDW2020** is a sample data warehouse provided by Microsoft, designed for learning and demonstrating data warehousing, ETL processes, and business intelligence. It uses a **star schema** with fact and dimension tables, modeling a fictional company that sells bicycles. Key components include **FactInternetSales** and **FactResellerSales** for sales data, and dimensions like **DimCustomer**, **DimProduct**, and **DimDate**. It supports analysis of sales trends, customer behavior, inventory management, and financial reporting, making it ideal for SQL, ETL, and BI practice.

I use Power BI to make this report. First, I connect PowerBI to load data from SQL server and then transform data. The data includes the following tables: DimEmployee, DimEmployeeSalesTerritory, DimProduct, DimResaeller, DimSalesTerritory, FactResellerSales. In addition, I also connect two more CSV files: ColorFormats and ResellerSalesTargets. After loading the data, I transform the data in Power Query Editor. Rename the tables in turn: DimEmployee to Salesperson, DimEmployeeSalesTerritory to SalespersonRegion, DimProduct to Product, DimResaeller to Resaeller, DimSalesTerritory to Region, FactResellerSales to Sales, ResellerSalesTargets to Targets. Merge the Product table and the ColorFormats table and use only the Product table. 

The next step is the data model part.
![image](https://github.com/user-attachments/assets/1a93c016-3927-4394-8de9-5b5d0ee78f3e)
In this step, I perform operations such as hiding some columns, creating a copy of the Salesperson table named Salesperson (Perfomance) {one table is related to the Sales table, the other table is related to the Region table, the reason is because 1 salesperson can manage many stores in different regions, doing so will help calculate the total revenue more accurately}. Next create date table, and creating relationships between table,...

The next step is to create DAX. Perform basic DAX creation such as calculating Profit and Profit Margin. Practice some measurements to gain a deeper understanding of the CACULATE function. Create measure time intelligence like Sale YoY Growth and Sales YTD

Next is the report design step
![image](https://github.com/user-attachments/assets/62291086-3b85-4fb0-859b-4056060e771e)



