# Vine_Review_Analysis


<h3> Overview Of The Analysis </h3>

Amazon vine service is a program where select amazon customers are supposed to post honest opinions and reviews about new as well as pre-release items to help fellow customers make informed decisions. On the other hand the Vine program allows manufacturers and publishers to receive reviews for their products. For a small fee, SellBy is participating in Amazon Vine program and providing products to Amazon Vine members, who will then publish a review about the products.

Verifying the authenticity of the vine program is the main purpose of this analysis. Amazon Vine review dataset is analyzed for vine vs non-vine: total reviews, 5-star reviews and percentage of the 5 star reviews, in order to assess the effectiveness of the Vine program. 

The ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin was performed using Pyspark. PySpark is then used to determine if there is any bias toward favorable reviews from Vine members in the Amazon_Reviews_Pet_Products dataset.


<h3>Resources</h3>

**Dataset**: Amazon Review Datasets: [amazon_reviews_us_Pet_Products_v1_00.tsv.gz](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Pet_Products_v1_00.tsv.gz) <br>
**Software:** Pyspark <br> 
**IDE:** Google Colab Notebook <br> 
**RDBMS**: PostgreSQL


<h2> <p align=center>Results </p></h2>

There is a bulleted list that addresses the three questions for unpaid and paid program reviews (7 pt)


<h2> <p align=center>Summary </p></h2>

The summary states whether or not there is bias, and the results support this statement (2 pt)
An additional analysis is recommended to support the statement 
