---
layout: post
title: What's ETL Process?✍️
subtitle: All about moving and manipulating datasets!
gh-repo: May30Sal/may30sal.github.io
gh-badge: [star, fork, follow]
cover-img: /assets/img/cover-2024-01-22.jpg
thumbnail-img: /assets/img/icon-2024-01-22.jpg
share-img: /assets/img/cover-2024-01-22.jpg
tags: [ETL Process. Database. Data.]
comments: true
author: Mayara Saldanha
---

ETL stands for **Extract - Transform - Load**. It's the process where we *extract* data from a data source (like a database), *transform* it depending on the needs, and *load* it into a destination source (like a data warehouse).

ETL processes are important because they allow to get, sort, organize and manipulate data from different data sources, making them available in only one repository, and letting them ready to be used by data analysts.

- **Extract Phase:** we select the data sources from where the data will be extracted. The data can be a table, an entire dataset, or a specific type of records.
- **Transform Phase:** we clean, organize and select the data that is needed. By removing duplicates, checking formatting patterns and unit conversions (for things like dates and measurements, for example) we ensure data integrity, and prepare the dataset to be analyzed.
- **Load Phase:** it's the last phase, when we load the newly transformed data into its final destination, that can be a database, a data lake or a data warehouse.

There is also a variation of this process that is called ELT. In this one, there is an inversion of the phases and the transformation occurs as a final step, being developed as needed.

<div style="font-size:2rem;width:100%;text-align:center;">
<img 
  align="center" 
  style="width:60%; height:60%; border: .25em solid #00bfa5; "
  src="/assets/img/img-2024-01-22.jpg" 
  alt="data icons image">    
</div>

To learn a little bit more about ETL Process I took the Udemy crash course [ETL using Python: from MySQL to BigQuery](https://www.udemy.com/course/etl-using-python-mysql-to-bigquery/). It has a "hands on" approach, using tools like MySQL, Python, Pandas, and BigQuery.

It was very important for me to be able to do the entire ETL process and see how it works in practice. To start, I established a connection with the database using a python script, and for this I learned how to create a virtual machine with Anaconda. I also imported the necessary modules, wrote some queries to get the data I needed, and reused some datasets that I had previously developed for a SQL Course.

For the transformation part, I learned how to use pandas and python functions to interact with the database, creating new columns and filtering the desired information. Then I exported the transformed data as .csv files. Finally, I loaded the data into BigQuery, using google cloud module to establish the connection with the data warehouse. 

And that was the first step of my wonderful journey into the data engineering field 🥳. All the activities developed during this project can be found in my Github repository [ETL_Process_MySQL_to_BigQuery](https://github.com/May30Sal/ETL_Process_MySQL_to_BigQuery) 


*All images by Freepik.*
