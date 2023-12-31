# MLP-81 - Building Data Pipelines with pandas, pyspark sql and polars.
- Dataset = https://www.kaggle.com/datasets/robikscube/flight-delay-dataset-20182022/Combined_Flights_2022.parquet
- Each of these libraries has its own strengths and use cases, so let's explore when to use each one:

# Pandas:

- Use Pandas when you're working with relatively small to medium-sized datasets that can fit comfortably in memory.
- Small datasets typically range from a few kilobytes (KB) to a few megabytes (MB).
- Examples might include simple spreadsheets, small CSV files, or small text files.
- Range: Less than 1 MB
- Example: 100 KB CSV file. 
- Pandas is great for data manipulation, exploration, cleaning, and transformation. It provides an intuitive DataFrame structure that is similar to working with tables in a relational database.
- It's well-suited for data analysis and visualization tasks, as it integrates well with other data visualization libraries like Matplotlib and Seaborn.

# Polars:

- Use Polars when you're working with medium-sized datasets and need fast data processing capabilities, especially for operations like filtering, aggregations, and joins.
- Medium-sized datasets can range from several megabytes (MB) to a few gigabytes (GB).
- Range: 1 MB to 1 GB
- Example: 500 MB database extract
- Examples could be moderate-sized CSV files, medium-sized database extracts, or JSON files. 
- Polars is designed to perform operations on in-memory data efficiently by leveraging Rust's performance optimizations. This can make it faster than Pandas for certain operations.
- It's a good choice for scenarios where you need to process data quickly and want to take advantage of parallel processing.

# PySpark:

- Use PySpark when you're dealing with large-scale datasets that cannot fit in memory on a single machine.
-  Large datasets generally start in the gigabyte (GB) range and can extend to terabytes (TB) or even petabytes (PB) in extreme cases. Range: 1 GB to 1 TB or more
- Example: 2 TB log file
- Examples might include massive log files, large-scale scientific datasets, or datasets generated by high-throughput sensors.
- PySpark is built on top of Apache Spark, a distributed computing framework. It's designed to handle big data processing and can scale out to clusters of machines, allowing you to process massive datasets in parallel.
- PySpark is suitable for tasks like distributed data processing, machine learning at scale, and processing streaming data.

# In summary:

If your dataset is small to medium-sized and fits in memory, use Pandas for its simplicity and rich ecosystem of tools.
If you're working with medium-sized datasets and need faster processing, consider using Polars for its performance optimizations.
If you're dealing with large-scale datasets that require distributed processing, PySpark is the way to go.
Keep in mind that the choice of library also depends on your familiarity with the library, your team's expertise, and the specific operations you need to perform on your dataset. It's always a good practice to try out different libraries and assess their performance for your specific use case before making a final decision.
