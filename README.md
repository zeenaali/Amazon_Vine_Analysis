# Amazon_Vine_Analysis

_Analysis with Pyspak and AWS_

Note: Password from Amazon_Reviews_ETL.ipynb file is deleted for safety reason. File needs pgAdmin password in order to run.

Project Overview
For this project I am using Amazon’s cloud service AWS, Google Colab and Pyspark to analyze Amazon’s reviews for outdoor products. The purpose of this analysis is to determine if there is any bias toward favorable reviews from Vine members. Amazon Vine program is a service that allows manufacturers to have reviews posted on Amazon for their pre-release items, for an additional fee.

## Resources

**Data Source**

- Amazon Vine Reviews for outdoors items

**Software:**

- Google Colab Vine_Review_Analysis.ipynb
- PgAdmin
- AWS Amazon_Reviews_ETL.ipynb

**Languages:**

- pySpark

## Results

In this analysis I analyzed reviews that have more than 20 total votes and the percentage of helpful votes is equal or greater than 50.

_How many Vine reviews and non-Vine reviews were there?_

There were

- 107 Vine reviews and
- 39,869 non-Vine reviews.

![image](https://user-images.githubusercontent.com/99419112/173274932-67c81381-c967-450a-a565-756ad68d153b.png)

  Figure 1: Total Vine and non-Vine reviews.

_How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?_

There were

- 56 five stars Vine reviews and
- 21,005 five stars non-Vine reviews.

![image](https://user-images.githubusercontent.com/99419112/173275031-e07a0911-b975-4ab9-87ae-05e7353cfca9.png)

    Figure 2: 5-star Vine and non-Vine reviews.

_What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?_

- 52.34 % of Vine reviews were 5 stars and
- 52.69 % of non-Vine reviews were 5 stars.

![image](https://user-images.githubusercontent.com/99419112/173275144-ddccf897-097f-460c-a55f-aaf96a4b8101.png)

     Figure 3: Percentage of 5-star Vine and non-Vine reviews.


## Summary
The purpose of this analysis is to analyze and determine if there is any bias toward favorable reviews from Vine members in the dataset. I analyzed reviews that have more than 20 total votes and the percentage of helpful votes is equal or greater than 50. This selection was made in order to pick reviews that are more likely to be helpful.

**Positivity bias for reviews in the Vine program**

In the analysis I analyze 5-star reviews within conditions mentioned above. Calculations show that there is no positivity bias for reviews in the Vine program. The results show that percentage of 5 stars Vine reviews is 52.34% and percentage of 5 stars non-Vine reviews is 52.69%. Non-Vine reviews have slightly higher percentage of the 5 stars reviews, 0.35% percentage points to be exact.

**Additional analyses and suggestions**

We could expand this analysis by calculating percentage for all stars reviews. Based on the results (Figure 4), there is a larger difference in percentage for 1-star reviews than for 5-stars reviews. Vine reviews have only 0.93% of 1-star reviews, while non-Vine reviews have 13.35 % 1-star reviews within conditions mentioned above. Similarly, there is 1.87% 2-stars Vine reviews and 6.05% 2-stars non-Vine reviews.


![image](https://user-images.githubusercontent.com/99419112/173275265-85a535e6-7045-4136-9081-06b0ccd816ee.png)

Figure 4: Summary table for all star reviews.

The results show that there could be positivity bias for reviews in the Vine program, when looking from 1 and 2-star reviews perspective.

Additionally, I would suggest another analysis beyond the given dataset. Non-vine reviews outnumber Vine reviews for 37,260 % (in this dataset, within certain conditions). In this case Vine reviews won’t affect the overall rating of the items. On Amazon site for Vine reviews https://www.amazon.com/gp/vine/help we can find explanation about the Vine program. The first sentence states: “Amazon Vine invites the most trusted reviewers on Amazon to post opinions about new and pre-release items to help their fellow customers make informed purchase decisions (1).” Vine reviews could have impact on newly released items sold on Amazon. For the manufacturers might be beneficial to have some reviews posted when launching their newly released products. At this point I would suggest to perform analysis on items that are similar (one group with Vine reviews and the other without) and measure sales increase over time. Based on that we could observe if Vine reviews contributed to faster increase of the sales of newly released items.
