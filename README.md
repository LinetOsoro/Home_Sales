# Home Sales Analysis with SparkSQL

## Introduction
In this module, SparkSQL is utilized to determine key metrics about home sales data. Temporary views are created, the data is partitioned, and temporary tables are cached and uncached for analysis purposes.

## Data Loading and Preparation
The home sales data is initially loaded from a CSV file into a Spark DataFrame. Subsequently, a temporary table named `home_sales` is created.

## Key Metrics Analysis
Several key questions are answered using SparkSQL:

1. **Average Price for Four-Bedroom Houses by Year**
   - Calculation of the average price for a four-bedroom house sold for each year.

2. **Average Price of Homes by Year Built with Specific Criteria**
   - Determination of the average price of homes for each year the home was built, with specific criteria such as three bedrooms and three bathrooms.

3. **Average Price of Homes per "View" Rating with Average Price ≥ $350,000**
   - Calculation of the average price of homes per "view" rating having an average home price greater than or equal to $350,000.

## Caching and Performance Comparison
The `home_sales` temporary table is cached, and its cached status is checked. Following that, the runtime of a query is compared with and without caching.

## Data Partitioning
The formatted Parquet home sales data is partitioned by the "date_built" field, and a temporary table for the Parquet data is created. The runtime of a query is then assessed with and without caching.

## Conclusion
The `home_sales` temporary table is uncached, and its uncached status is verified using PySpark.

## GitHub Repository
The code can be found in the Home_Sales.ipynb file, available in the "Home_Sales" GitHub repository.
