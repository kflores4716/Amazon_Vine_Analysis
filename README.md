# Amazon_Vine_Analysis

## Overview

The goal of this analysis is to comb through some Amazon reviews that were written as part of their Vine program and determine if there is any evidence of bias. As some reviewers were getting paid and others were not, we want to see if there is a noticeable difference between those two groups and how they reviewed their purchases. We pulled our data from a list of publicly available US Amazon reviews datasets and used `PySpark` and an `Amazon Web Services RDS` to complete the analysis. The data set we chose was the Sports data set, available at the following url: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Sports_v1_00.tsv.gz.


## Results

Once we completed our Analysis, we found some interesting results. While our outcome can't really apply to ALL Amazon reviews (there are so many), it does offer guidance when considering a possibility of bias in the Amazon Vine program. The results are as follows:

### Count of Total Reviews

##### Vine Reviews

![paid_vine_df](https://user-images.githubusercontent.com/94764735/163274427-42ae8ec2-125a-43e0-ba3c-c4050ff2b23b.png)

![paid_vine_count](https://user-images.githubusercontent.com/94764735/163274491-13dcbdb2-ea5f-4b3c-acb9-17d1531886d1.png)

- The total number of Vine reviews was 334


##### Non-Vine Reviews

![unpaid_vine_df](https://user-images.githubusercontent.com/94764735/163274546-90d2e33d-ce77-4556-a5db-1921509ace45.png)

![unpaid_vine_count](https://user-images.githubusercontent.com/94764735/163274562-b3e97e96-f340-418b-bd49-1266e44d4bbb.png)

- The total number of Non-Vine reviews was 61,614


### Count of 5-star Reviews

##### Vine Reviews 

![paid_5star](https://user-images.githubusercontent.com/94764735/163274872-f1055222-a227-48a3-b337-6e93fb2c820e.png)

- The number of 5-star Vine reviews was 139

##### Non-Vine Reviews

![unpaid_5star](https://user-images.githubusercontent.com/94764735/163274882-ee7470eb-6aa2-407b-881b-28d12a09744b.png)

- The total number of 5-star Non-Vine reviews was 32,665


### Percentage of 5-star Reviews

##### Vine Reviews

![paid_5star_percent](https://user-images.githubusercontent.com/94764735/163274986-d6472d3e-50f1-4a22-b9cd-c7c361a016f1.png)

- The percentage of 5-star reviews amongst all Vine reviews was 41.62%

##### Non-Vine Reviews

![unpaid_5star_percent](https://user-images.githubusercontent.com/94764735/163275002-b302e2a9-904d-4e47-859e-bbc4f1c4bc86.png)

- The percentage of 5-star reviews amongst all Non-Vine reviews was 53.02%


## Summary

According to this data set, there does not seem to be a bias when comparing the paid reviews to non-paid reviews (at least not how we expected). The bias we are looking for is whether the paid reviewers are giving more 5-star reviews than those who aren't paid. It would make sense for them to give, on average, higher reviews if they are getting paid to do so. However, from our analysis we found that the 5-star review rate is actually lower for those paid reviewers. At 41.62%, the rate of 5-star reviews is almost 12% lower for paid reviewers than the 53.02% rate from the unpaid.

It was a bit surprising to find that the paid reviewers on average gave lower reviews. If anything, we would think these percentages would be switched around. You would think that Amazon (or the third party vendor) would only be inclined to pay for good reviews in order to make the product more desirable, but clearly that might not always the case. Still, it would be a good idea to further analyze this data to get a better understanding of why this discrepancy exists. Looking at the split of these reviews, there are far more unpaid reviews than paid, so an immediate possibility that you might think of is that some of the unpaid reviews were written by bots or by people who never actually bought and used the product. Perhaps the vendor paid for more 5-star reviews on their own agenda, separate from the vine program. To get a better understanding of how likely this is, we could perform a similar analysis with the 1,2,3, and 4-star reviews to see how they split up. If the percentage of 3 to 4-star reviews are similar between paid and unpaid, perhaps the vendor actually did pay for fake reviews. Sometimes all a vendor needs is a little 1-star increase in average rating to sell more of their product, and paying for extra 5-star reviews (even if they're fabricated) can accomplish just that. 


