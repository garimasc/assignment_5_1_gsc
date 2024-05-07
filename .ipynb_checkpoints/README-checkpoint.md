# Assignment 5.1: Will a Customer Accept the Coupon?
 
## Overview
In this project, we look at Amazon Mechanical Turk survey data that comes to us via the UCI Machine Learning repository. A coupon is delivered to the cell phones of drivers when they are in the vicinity of a restaurant, and the data records their response: if they accepted to use it right away, save it for a later date or declined the coupon. Additionally, we have access to a variety of other information such as personal and demographic information of the driver, type of coupon, weather, destination, and so on. Our goal here was to use our current knowledge of plotting and visualizations to highlight differences between who did or did not accept a coupon offering.

## Analysis
### Investigating and Cleaning Data
The first step was to load the data, and investigate it for any missing/problematic values. There were a few mistakes in spellings which we have ignored at this stage. But the main steps in this direction were:

1. _'Car'_ column is missing 99% of the values - we are going to ignore this in any analysis due to sparsity of information.
2. _'Bar'_, _'CarryAway'_, etc. columns, which record the frequency of visit, are missing 1-2% of the values. We decided to drop these rows from our analysis.
3. Edit the _'coupon'_ columns to make sure the spellings match with the column names that record frequency of visit. For example, 'Restaurant(<20)' becomes 'RestaurantLessThan20'. This is in order to make the charts and data easier to interpret.
4. Customers with no specific driving destination have been marked as driving in opposite direction to the coupon venue. We believe this is incorrect and will skew the results. Hence we added a new _'Direction'_ column with 3 possible values: Same, Opposite and NA.

### Results
Based on the prompts provided in the starter notebook, we looked at the different factors that might affect the chances of a coupon being accepted. The first few things that we looked at were the driving direction, distance to coupon venue, age of customer, and the weather. 

**Longer distance to coupon venue decreases chances of acceptance**
<img src="images/distance_to.png">

**Customers more likely to accept coupons when the weather is good**
<img src="images/weather.png">

## Conclusion and Next Steps

We have clearly identified that there is no single factor that can help us accurately determine the probability of a coupon being accepted.


