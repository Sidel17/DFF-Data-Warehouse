# DFF-Data-Warehouse
# Project Team
Aditya Wagholikar
Prashant Shisodia
Karen Xu

# Summary 
This is a repository for the data warehouse project of Dominic Finer Food(DFF). Created staging and data warehouse area  using MS SQL server 2016. Performed ETL using SSIS, created reports using Report Builder 3.0 , SSAS and SSRS.
5 critical business questions are answered in this project for the retail chain.

## Schema Design

![image](https://user-images.githubusercontent.com/4469379/44959165-18e5f180-aeb0-11e8-956d-de7b8bff348c.png)

![image](https://user-images.githubusercontent.com/4469379/44959205-8134d300-aeb0-11e8-98b4-ca1451ead58c.png)

# Business Questions

## BQ-1: What is the trend of weekly change in sales of Frozen Food, Meat, Fish and Dairy till current week in 1997 for store 2?

Justification – This business question is answered by Category Sales data mart. The Store Number attribute is used from Store dimension table to divide the data by Store. The week number and year attribute are used from Time dimension table to further divide data. The Category name attribute is used from Category dimension table to divide data in frozen meat, fish and dairy food category. The measure Category_sales from the Category Sales fact table is used to find the trend of weekly change in sales of Frozen Food, Meat, Fish and Dairy till current week in 1997 for store 2.

Product Sale Data Mart helps to resolve BQ-2 – BQ-5.

## BQ-2: Which are the top 10 products with respect to profitability in Medium Tier stores w.r.t “Canned Soup” category of in year 1991?
Justification - This business question is answered by ProductSales data mart. We have used store_tier attribute from Store dimension table and year from Time dimension table as filters. Product details like UPC and Name is taken from Product dimension table. The measure Gross_Total is taken from Product Sales fact table and summed for given products and ranked. We display the top 10 products by applying rank function.

## BQ-3: What is the growth trend of Soft Drinks versus Bottled Juice for year 1990 and 1991? Which of these has negative growth rate? What is the trend for bottled juice especially in Low Tier?
Justification - This business question is answered by Product Sales data mart. We have used store_tier attribute from Store dimension table, year from Time dimension table. Year filter acts as a filter criterion. The measure Gross_Total is taken from Product Sales fact table and summed for given years. We display the total sales growth with respect to previous year for product type combination.

## BQ-4: What effect does the time of the year have on sales of each Tuna? Determine the impact of seasonality on Average Sales of Tuna from December-1990 to September 1992?
Justification - This business question is answered by ProductSales data mart. We have used year attribute from Time dimension table to filter on the basis of year. Month and Week attributes from Time dimension table are used to measure time dimension against which we plot average of Sales. Sales attribute comes from Product Sales Fact table.

## BQ-5: What is annual growth rate of cigarette margins in low tier stores? What is the decreasing trend?

Justification - This business question is answered by Product Sales data mart. We have used store_tier attribute from Store dimension table to filter. Year attributes from Time dimension table are used to measure time dimension against which we plot sum of Gross_Margin.
Gross_Margin comes from the data mart - Product_Sales. Store_Num attribute comes from Store dimension table. We show a store wise trend plotted against year.




