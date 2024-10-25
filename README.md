**AdventureWorksDW2020** is a sample data warehouse provided by Microsoft, designed for learning and demonstrating data warehousing, ETL processes, and business intelligence. It uses a **star schema** with fact and dimension tables, modeling a fictional company that sells bicycles. Key components include **FactInternetSales** and **FactResellerSales** for sales data, and dimensions like **DimCustomer**, **DimProduct**, and **DimDate**. It supports analysis of sales trends, customer behavior, inventory management, and financial reporting, making it ideal for SQL, ETL, and BI practice.

I use Power BI to make this report. First, I connect PowerBI to load data from SQL server and then transform data. The data includes the following tables: DimEmployee, DimEmployeeSalesTerritory, DimProduct, DimResaeller, DimSalesTerritory, FactResellerSales. In addition, I also connect two more CSV files: ColorFormats and ResellerSalesTargets. After loading the data, I transform the data in Power Query Editor. Rename the tables in turn: DimEmployee to Salesperson, DimEmployeeSalesTerritory to SalespersonRegion, DimProduct to Product, DimResaeller to Resaeller, DimSalesTerritory to Region, FactResellerSales to Sales, ResellerSalesTargets to Targets. Merge the Product table and the ColorFormats table and use only the Product table. 

The next step is the data model part.
![image](https://github.com/user-attachments/assets/1a93c016-3927-4394-8de9-5b5d0ee78f3e)
In this step, I perform operations such as hiding some columns, creating a copy of the Salesperson table named Salesperson (Perfomance) {one table is related to the Sales table, the other table is related to the Region table, the reason is because 1 salesperson can manage many stores in different regions, doing so will help calculate the total revenue more accurately}. Next create date table, and creating relationships between table,...

The next step is to create DAX. Perform basic DAX creation such as calculating Profit and Profit Margin. Practice some measurements to gain a deeper understanding of the CACULATE function. Create measure time intelligence like Sale YoY Growth and Sales YTD

Next is the report design step
![image](https://github.com/user-attachments/assets/62291086-3b85-4fb0-859b-4056060e771e)

Sales and Profit Margin by Month
  The highest sales occurred in September 2019, and there was a dip in sales in January 2020.
  Profit margin shows slight fluctuations, with a decrease towards May 2020.
  => Sales Trends: September 2019 saw peak sales, but there was a significant dip in early 2020.

Sales by Country and Category (Accessories, Bikes, Clothing, Components). 
  United States has the largest share of sales, dominated by Bikes.
  Other countries like Canada, France, and the United Kingdom show much lower sales.
  Germany and Australia show very small sales contributions.
  =>The United States dominates sales, especially in the Bikes category, while other countries contribute less.

Quantity by Category
  Clothing leads in terms of quantity, followed closely by Bikes.
  Components and Accessories have significantly lower quantities sold.

Drill through Product Detail
![image](https://github.com/user-attachments/assets/80753e2f-9d45-4f19-98d2-cbe29727db6b)
Mountain Bikes perform the best in terms of profitability, especially with the black and silver models showing healthy profit margins.
Road Bikes and Touring Bikes, while generating significant revenue, suffer from negative profit margins across all colors, with some of the worst losses in the yellow models of both subcategories.
Attention may be required to adjust pricing or costs for Road and Touring Bikes to improve profitability.

Profit
![image](https://github.com/user-attachments/assets/54c7c2ff-003f-43a9-93fe-dd8d94a5d959)
FY2020 had much higher sales than FY2019, but profitability took a significant hit, indicating rising costs or inefficient pricing strategies.
FY2020Q1 was the most problematic quarter, with high sales but the biggest loss, likely due to disproportionately high costs.
While FY2020Q2 and FY2020Q3 had slight recoveries, the company was still struggling to achieve meaningful profit margins.

My Performance
![image](https://github.com/user-attachments/assets/4d0e79e0-2d74-4872-a5d2-28918093c34d)
![image](https://github.com/user-attachments/assets/acd369f9-d238-4771-af5f-4eda77fd1b6d)
There was a strong start in the fiscal year, with several months outperforming the targets.
A downturn began in the early months of 2020, with targets being missed, particularly in March through May.
The variance margin overall is positive (+14.80%), meaning that despite some months underperforming, the fiscal year as a whole exceeded the sales target.

Scatter Chart

https://github.com/user-attachments/assets/34d575d7-ab4a-486b-bcfc-5b3be498bdec

This chart can be useful to understand how different business types are performing in terms of sales and profitability during 2019, 2020.

Forecast 
![image](https://github.com/user-attachments/assets/1d1dc24a-5af2-469a-8569-06f0ec626622)
This chart can help identify patterns in sales activity, detect seasonal trends, and highlight periods of significant growth or volatility.
  
