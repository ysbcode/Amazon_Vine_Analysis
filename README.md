# Amazon_Vine_Analysis

## Project Overview

Analyzing Amazon reviews. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products.
In this project, you’ll have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. 
You’ll need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, 
and load the transformed data into pgAdmin. Next, you’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset.

### Resoursces Used

 - Google Colab Notebooks for PySpark
 - AWS and pgAdmin for cloud RDS
 - [Amazon Review Datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)

### Deliverable #1

This project analyzes Amazon Vine program and determines if there is a bias toward favorable reviews from Vine members. For the first part of the project, created a cloud relational database using Amazon Web Services (AWS) and connected our database using a PostgreSQL. We then created four tables in our RDS using the [schema](https://github.com/shahkibria/Amazon_Vine_Analysis/blob/main/ETL_schema.sql) provided. Finally, we extracted Amazon review dataset regarding video game reviews, transformed the data based on the directions provided for the Challenge and then uploaded the data into our cloud database tables. We used postgreSQL to create our tables and PySpark for the ETL process. As evidence, we have included screenshots for the dataupload in this repository. Our Code for the ETL process is also included in this repository.

![](https://github.com/ysbcode/Amazon_Vine_Analysis/blob/main/Screenshots_Data%20Import/review_id_table.PNG?raw=true)

![](https://github.com/ysbcode/Amazon_Vine_Analysis/blob/main/Screenshots_Data%20Import/products_table.PNG?raw=true)

![](https://github.com/ysbcode/Amazon_Vine_Analysis/blob/main/Screenshots_Data%20Import/customers_table.PNG?raw=true)

![](https://github.com/ysbcode/Amazon_Vine_Analysis/blob/main/Screenshots_Data%20Import/vine_table.PNG?raw=true)

### Deliverable #2

For the second deliverable, we again extracted video game Amazon review datasets and loaded the data into a new GoogleColab notebook using PySpark. We filtered the data to only include games where total reviews received were greater than 20. We then further filtered the data to include games where the proportion of helpful votes to total is greater than or equal to 50%. Finally we divded the dataset into two groups: reviews given as part of the vine program(paid) and reviews given oustide the vide program(unpaid). 
Using the two datasets, we compared the ratio of proportion of 5-star reviews to total reviews between reviews obtain from the vine program and reviews outside the vine program. Our Vine Analysis Code for this exercise is also included in this repository.  

## Result of our analysis

When comparing 5-star ratings between the two datasets, we noted that the proportion of 5-star ratings in the Vine program is around 51% while the proportion of 5-star ratings in reviews outside the vine program drops to 38.7%. A screenshot of our result is provided below. 

![](https://github.com/ysbcode/Amazon_Vine_Analysis/blob/main/Screenshot_Data%20Analysis/Amazon_vine_analysis.PNG?raw=true)

## Summary

As we can see, there is a significant increase in 5-star reviews (almost 12%) when reivews are obtained from the Vine Program. This suggests a positive bias for reviews within the vine program. 

We could however perform further analysis into this data. We could compare the proportion of all the ratings instead of only focusing on 5-star ratings. We could then provide a better picture on whether a bias exists accross all ratings and not just the top rating. We could also compare the average rating within the two data sets (vine and not vine) to determine if there is a general probability of reviewers providing better reviews within the vine program. 

