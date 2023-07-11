# ETL_tool
![ssis_package](https://github.com/korneldata/ETL_tool/blob/cccaf64bf071f695c26fa38de7d5c9b60ffa11a4/ssis_package.png)

#Project overwiew:

I developed ETL (Extract, Transform, Load) tool which:

Data Flow 1:
1) Load csv file containing regional reports from folder using Flat File Source,
2) Convert data types using Data Conversion task,
3) Calculate total_sales using Derived Column task,
4) Calculate operating_profit using Derived Column task,
5) Iterate through each file in folder performing above tasks (using Foreach Loop Container),
6) Load data from all csv files to existing data in SQL database,

Data Flow 2:
1) Generate performance report for all regions in 2021 with SQL query using GROUPING SETS,
2) Load created report to file in folder.

#Used technologies:

SQL Server Integration Services (SSIS) in Microsoft Visual Studio 2022

