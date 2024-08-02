# Module 22 - SparkSQL Challenge
Home Sales - SparkSQL Challenge - Week 22 - Data Analytics Boot Camp - University of Oregon

![SparkSQL Challenge](images/project_banner.jpg)

## Background
I'm using SparkSQL to determine key metrics about home sales data. I used Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## Approach
This project was initially created as a [Google Colab project](https://colab.research.google.com/drive/1EWoheGOa2-MJ4qfTVcoyKXrHzp85ceXm?usp=sharing). A copy has been downloaded to GitHub for easy reference.


- Import the necessary PySpark SQL functions
- Read the home_sales_revised.csv data from an S3 bucket and into a Spark DataFrame.
- Create a temporary table.
- Answer the following questions using SparkSQL:
    - What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
    - ![](images/3_avg-price-per-year_4bed.JPG)
    - What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
    - ![](images/4_avg-price-per-year_3bed3bath.JPG)
    - What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
    - ![](images/5_avg-price-per-year_3bed3bath2floor2000sqft.JPG)
    - What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.
    - ![](images/6_avg-price-views_350000plus.JPG)
- Cache a temporary table and confirm it has been cached.
- Using the cached data, run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. - Determine the runtime and compare it to uncached runtime.
    - **Uncached Runtime:**  0.7048161029815674 seconds
    - **Cached Runtime:**  0.568709135055542 seconds
- Partition by the "date_built" field on the formatted parquet home sales data.
- Create a temporary table for the parquet data.
- Run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
    - **Uncached Runtime:**  0.7048161029815674 seconds
    - **Parquet Runtime:**  1.135207176208496 seconds
- Uncache the home_sales temporary table and verify it was uncached using PySpark.
