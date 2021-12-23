# Amazon_Vine_Analysis
Using PySpark on Google Colab with AWS RDS PostGres and S3 to identify bias toward favorable reviews from Vine members 

## Overview of the analysis: 
The purpose of this analysis was to determine if there is any bias towards reviews that were written as part of the Vine program. The Vine program is a program ran by Amazon that that invites the most trusted reviewers to post opinions about new products.  These reviewers are sometimes provided free products by the participating sellers to help bring customer awareness to new offerings.

The data was first stored in an AWS Postgres database via PySpark and then retrieved back into a Spark Dataframe as seen below.

![alt text](https://github.com/jj2773/Amazon_Vine_Analysis/blob/main/vine_df.PNG)

It was desired to then filter only reviews with more than 20 total votes and a helpful votes ratio of 50% or more.

Refrencing the summary data below some observations can be mode from the data

* There was a total of 47 vine reviews and 8362 non-vine reviews.
* The number of 5 star ratings from vine members was 15 while the non-vine members gave 4332 5 star ratings.
* Therefore the percentage of 5 Star Ratings for vine members was 32% versus 52% for non-vine members

![alt text](https://github.com/jj2773/Amazon_Vine_Analysis/blob/main/vine_vs_nonvine_5star_ratings.PNG)


## Summary
There doesn't seem to be any positivity bias for reviews in the Vine program for the watches data since the 5 star rating percentage is much lower at 32% versus non-vine member ratings of 52%.  An additional analysis that could be performed is to look at another dataset since the quantity of vine reviews was not very large for watches.

