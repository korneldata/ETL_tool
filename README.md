# ETL_tool
SQL query to generate performance report for regions in 2021:

SELECT 
	 DATEPART(month, sales_date) as "month",
	 DATEPART(year, sales_date) as "year",
	 region,
	 sum(operating_profit) as total_profit
FROM report
WHERE DATEPART(year, sales_date) = '2021'
GROUP BY 
GROUPING SETS (
	(DATEPART(month, sales_date), DATEPART(year, sales_date), region),
	(DATEPART(year, sales_date))
)
ORDER BY "month"
