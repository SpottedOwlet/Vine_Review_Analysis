#  <p align=center> Vine_Review_Analysis </p>


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
<br>

- **Total Number of Reviews:**

  <h4><p align=center> Paid vs Unpaid </p></h4>

<kbd>
  <img width="1174" alt="Screen Shot 2022-02-20 at 12 37 35 PM" src="https://user-images.githubusercontent.com/90424752/154878807-aca8cc3d-c3a1-435d-a37d-a51dad6a0a54.png">
    
</kbd>
<br>
<br>

The above image shows the total number of paid and unpaid reviews among the pet products Vine reviews dataset. <br>

<br>

- **Total Number of 5 start reviews:**

<h4><p align=center> Paid vs Unpaid </p></h4>

<kbd>

  <img width="1174" alt="Screen Shot 2022-02-20 at 12 37 54 PM" src="https://user-images.githubusercontent.com/90424752/154879330-3350ffc3-e070-4780-86e6-7609f06a6caa.png">

  
</kbd>
<br>
<br>

- **Percentage of 5 start reviews:**

<h4><p align=center> Paid vs Unpaid </p></h4>

<kbd>

<img width="1170" alt="Screen Shot 2022-02-20 at 12 38 20 PM" src="https://user-images.githubusercontent.com/90424752/154880405-ae0bcaa7-4e8d-455e-91e5-39b2b95bfe0d.png">

  
</kbd>
<br>
<br>

<h2> <p align=center>Summary </p></h2>

The dataset was first filtered for products with more than 20 votes. Then it was further filtered for paid and unpaid reviews. Then the percentages were found for vine and non-vine reviews. 

**Observation :** <br>

- The paid or vine reviews were only 162 out of total 35,730 reviews cosidered for this analysis.
- Although small in number, out of the total vine reviews, 38.88% reviews were 5-star reviews.
- From the unpaid or non-vine reviews, the percentage of 5-star reviews was 54.65%.

The above analysis does not reflect any positivity bias, however mere percentages can not accurately assess whether there is a positivity bias in the votes of Vine program.

Instead of calculating the percentages of 5-star ratings, comparing the **average star rating** for vine and non-vine reviews might be **a better measure of the positivity bias.**

<br>

<h4> <p align=center> Additional Analysis for positivity bias: </p> </h4>

<br>

<kbd>

<img width="1253" alt="Screen Shot 2022-02-20 at 11 57 52 PM" src="https://user-images.githubusercontent.com/90424752/154912257-df5597be-8649-43c3-88cc-f0ef5cc4c494.png">

</kbd>
<br> <br>

This additional step for positivity bias clearly indicates that on an average vine reviews contain more 4 and 5 star reviews than non-vine reviews. And hence, there is a greater chance that the vine reviews might be positively biased.
