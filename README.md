# Amazon_Vine_Analysis

## Overview
The purpose of this analysis is to analyze Amazon reviews written by members of the paid "Amazon Vine" program for the following dataset:

https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_02.tsv.gz

With this dataset, we used PySpark to perform the ETL process to extract and transform the data, connect to an AWS RDS instance, and then used PgAdmin to load the data. We then utilized PySpark to analyze whether there is any bias toward favorable reviews from Vine members. 


## Results
### How many Vine reviews and non-Vine reviews were there?
There were no paid reviews.
![image](https://user-images.githubusercontent.com/106359572/194780598-2596b5a1-ad5c-49fd-8e03-0bf6721b8c64.png)
![image](https://user-images.githubusercontent.com/106359572/194780648-6ba11f20-302c-4835-8f0d-a2c5101ad5e1.png)

### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
There were no vine reviews for any of the rating categories (see above).
There were 242,889 unpaid, 5-star reviews.

![image](https://user-images.githubusercontent.com/106359572/194780704-c095c2c1-7f92-4a6b-a99d-86106d369965.png)

### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
The count of total votes (all of which were upaid) was 403,807; the percentage of five-star reviews (all of which were unpaid) amounted to slightly over 60%

![image](https://user-images.githubusercontent.com/106359572/194780735-17284870-0266-47c0-a1c3-3e3bbbef579e.png)
![image](https://user-images.githubusercontent.com/106359572/194780724-19a51793-09d6-4e73-976c-49949039d0c3.png)


## Summary: 
It is not theorhetically possible to conclude with this particular dataset whether there is any positivity bias for reviews in the Vine program, since the number of paid reviews amounted to zero (out of a substantial 400K data rows). The analysis should be performed if possible on the other book review datasets, to better assess wehther this is typical with book reviewers, or whether the dataset in this case was exceptional/rare.  The csv files should also be combed for errors resulting in the null count of paid reviews.
