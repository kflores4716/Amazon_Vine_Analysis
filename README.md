# Amazon_Vine_Analysis

## Overview

The goal of this analysis was to comb through some reviews written as part of the Amazon Vine program to see if there is evidence of bias. We started by pulling a data set containing Amazon review information and placing it in a dataframe. Next, we filtered that dataframe into a table to get rid of the metrics we didn't need for our analysis. Using that new table, we furthere filtered according to `total_votes` and percentage of `helpful_votes` to make sure that we didn't have any data that will skew our analysis or cause errors later on (no zero-value rows). After cleaning our data, we separated the Vine reviews into 'Paid' and 'Unpaid'


The goal of this analysis is to comb through some Amazon reviews that were written as part of their Vine program and determine if there is any evidence of bias. As some reviewers were getting paid and others were not, we want to see if there is a noticeable difference between those two groups and how they reviewed their purchases. We pulled our data from a list of publicly available US Amazon reviews datasets and used `PySpark` and an `Amazon Web Services RDS` to complete the analysis. The data set we chose was the Sports data set, available at the following url: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Sports_v1_00.tsv.gz.


## Results

Once we completed our Analysis, we found some interesting results. While our outcome can't really apply to ALL Amazon reviews (there are so many), it does offer guidance when considering a possibility of bias in the Amazon Vine program. The results are as follows:

- **Count of Total Reviews**

#### Vine Reviews

![paid_vine_df](https://user-images.githubusercontent.com/94764735/163274427-42ae8ec2-125a-43e0-ba3c-c4050ff2b23b.png)

![paid_vine_count](https://user-images.githubusercontent.com/94764735/163274491-13dcbdb2-ea5f-4b3c-acb9-17d1531886d1.png)



#### Non-Vine Reviews

![unpaid_vine_df](https://user-images.githubusercontent.com/94764735/163274546-90d2e33d-ce77-4556-a5db-1921509ace45.png)

![unpaid_vine_count](https://user-images.githubusercontent.com/94764735/163274562-b3e97e96-f340-418b-bd49-1266e44d4bbb.png)




- **Count of 5-star Reviews**

#### Vine Reviews 

![paid_5star](https://user-images.githubusercontent.com/94764735/163274872-f1055222-a227-48a3-b337-6e93fb2c820e.png)


#### Non-Vine Reviews

![unpaid_5star](https://user-images.githubusercontent.com/94764735/163274882-ee7470eb-6aa2-407b-881b-28d12a09744b.png)




- **Percentage of 5-star Reviews**

#### Vine Reviews

![paid_5star_percent](https://user-images.githubusercontent.com/94764735/163274986-d6472d3e-50f1-4a22-b9cd-c7c361a016f1.png)


#### Non-Vine Reviews

![unpaid_5star_percent](https://user-images.githubusercontent.com/94764735/163275002-b302e2a9-904d-4e47-859e-bbc4f1c4bc86.png)






