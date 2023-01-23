# Amazon_Vine_Analysis

## Overview

Amazon's Vine program allows online shippers and manufacturers to receive reviews for their products when sold on Amazon. From this program we chose a sample dataset from their Sports reviews work with. A basic ETL process was performed to load the dataset into python and the data was tranformed and connected to the Amazon RDS with pgAdmin. Finally, PySpark was used to determine if there is any bias towards positive or favorable reviews of products from the Vine Members.

### Resources
* [Dataset:] (https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Sports_v1_00.tsv.gz)
* Software/Packages used: Google Colab notebooks, PySpark, pgAdmin, PostgreSQL, AWS. 

## Results

### Number of Reviews

![total nonvine reviews](/Resources/total_unpaid_reviews.png)

![total vine reivews](/Resources/total_paid_reviews.png)

As shown in the above images, there were 334 Vine reviews for the sports set, and 61614 non vine reviews.

![vine 5star](/Resources/vine_five_star.png)

![vine 5star percent](/Resources/paid_fivestar_percent.png)

Of the 334 Vine reviews, 139 were five star reviews, telling us that ~42% of the paid vine reviews gave the product 5 stars.

![unpaid 5star](/Resources/unpaid_fivestar.png)

![unpaid 5star percent](/Resources/unpaid_fivestar_percent.png)

Of the 61614 reviews not in the vine program, 32665 gave five stars, meaning that the non vine reviews had a higher percentage of five star reviews at ~53%.

## Summary

Given that there was a higher percentage of five star reviews in the non-paid review section, we can conclude that there is not a positivity bias in the vine program. To further support this evidence, we could calculate summary statistics for all of the reviews and compare the mean and median review scores from both the vine and non vine reviews.  