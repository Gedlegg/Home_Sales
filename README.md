# Spark SQL Home Sales Analysis Report

### **1. Overview**

This report summarizes the analysis of home sales data using Apache Spark. The dataset was processed using PySpark to answer specific queries related to average home prices based on various criteria. The analysis includes query results, runtime comparisons, and performance evaluations.

### **2. Setup and Data Ingestion**

* **Libraries Imported:**
  * `pyspark.sql.SparkSession`
  * `pyspark.sql.functions.avg`, `pyspark.sql.functions.round`
  * `time`
* **Spark Session Initialization:**
  * A Spark session named "Home Sales Analysis" was created.
* **Data Ingestion:**
  * The dataset was read from a CSV file located at `https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.2/22-big-data/home_sales_revised.csv`.
  * The data was loaded into a Spark DataFrame and registered as a temporary view named `home_sales`.

### **3. Queries and Results**

#### **Query 1: Average Price for Four-Bedroom Houses Sold Per Year**

* **Objective:** Calculate the average price of four-bedroom houses, grouped and ordered by year sold.
* **Output:** [Displayed Results]

#### **Query 2: Average Price of Homes with 3 Bedrooms and 3 Bathrooms by Year Built**

* **Objective:** Calculate the average price of homes with 3 bedrooms and 3 bathrooms, grouped and ordered by the year built.
* **Output:** [Displayed Results]

#### **Query 3: Average Price of Homes with Specific Criteria by Year Built**

* **Objective:** Calculate the average price of homes with 3 bedrooms, 3 bathrooms, 2 floors, and at least 2000 sqft living space, grouped and ordered by the year built.
* **Output:** [Displayed Results]

#### **Query 4: Average Price Per View Rating with Average Price >= $350,000**

* **Objective:** Calculate the average price of homes based on the view rating, including only those homes with prices greater than or equal to $350,000, grouped and ordered by view rating in descending order.
* **Runtime (Uncached):** [Runtime Result] seconds
* **Output:** [Displayed Results]

### **4. Performance Optimization**

#### **Caching the `home_sales` Table**

* **Action:** The `home_sales` table was cached to improve performance for repeated queries.
* **Check if Cached:** [Result]

#### **Re-run Query 4 Using Cached Data**

* **Runtime (Cached):** [Runtime Result] seconds
* **Output:** [Displayed Results]

**Comparison:** The cached query runtime was compared to the uncached runtime to assess performance improvement.

### **5. Data Persistence and Re-Analysis**

#### **Write DataFrame as Parquet Files**

* **Action:** Data was partitioned by `date_built` and written as Parquet files.
* **Path:** [Specify the path used]

#### **Re-run Query 4 on Parquet Data**

* **Runtime (Parquet):** [Runtime Result] seconds
* **Output:** [Displayed Results]

### **6. Table Uncaching and Session Termination**

* **Uncache Table:** The `home_sales` table was uncached.
* **Check if Uncached:** [Result]
* **Stop Spark Session:** The Spark session was terminated.
