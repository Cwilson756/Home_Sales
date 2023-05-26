# Home_Sales
My Repository for the Module 22 Challenge, Big Data Home Sales.

## The Project

For this project, I used PySpark SQL to create a Spark DataFrame from the home_sales_revised.csv. I then created a temporary table named home_sales to answer the following questions:

    What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

    What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

    What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

    What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.


After answering these questions, I cashed the temporary table and assured it was cashed. I then re-ran the final question from above with the cashed data to test the runtime difference. I found that the cashed data was much faster, coming in at ~.5 seconds to run compared to 1.5 seconds with the uncashed temp table.

I then formatted the home sales data into parquet home sales data, partitioning on the 'date_built' field and created a temporary table for this data. After re-running the final question answered above to compare runtimes, the parquet data ran slightly slower than the cashed data at ~.7 seconds runtime. However, compared to the previous uncashed data it ran about twice as fast.

Finally, I uncashed the home_sales temp table and verified it was uncashed.
