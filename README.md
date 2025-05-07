## PA5_1: Project on Likelihood and Characteristics of Drivers Accepting Coupons

_Link to corresponding Jupyter notebook: https://github.com/pamelakhalaf/PA5_1/blob/main/code/PracticalApplication1_coupons_PK.ipynb_

### Problem Statement 
This exploratory analysis is aimed at predicting whether a driver receiving a coupon on his cellphone as he/she is driving through town will accept it or not. Various types of coupons are offered (e.g. bar, coffee house, restaurant, carry out & take away) under different driving conditions, weather conditions, time of the day and locations.  


### EDA 
The data comes from the UCI machine learning repository and was collected through a survey on Amazon Mechanical Turk. The data consisted of 12684 entries for a total of 26 columns.  
The dataset does include missing values. In one instance, for the column "car", 99% of the column values was missing and the column was dropped. In other instances, < 2% of the dataset was missing and for those fields, we imputed with the most frequent value of that field. 
74 duplicates in the dataset were also dropped. 


### Analysis & Findings 
#### Coupons Offered 
The number of coupons offered was heterogenous across different types of coupons. Coffee house coupons were offered the most, whereas expensive restaurant ($20-$50) coupons were offered the least. 
When visualizing the driver attributes and driving conditions under which these coupons were offered, we see inconsistencies across different types of coupons. Knowing that some of these conditions could impact likelihood of coupon acceptance, we focus the analysis on each type of coupons instead of cross-comparing or generalizing findings from one coupon type. 
#### Findings for Each Type of Coupon
1. Bar coupons: Likelihood of a bar coupon being accepted is 41%. Drivers who accept the bar coupon tend to be ones that frequent bars at least once a month, with those going more than 4 times being very highly likely to accept the coupon. Additional driver characteristics that increase their likelihood of accepting include having passengers in the car other than kids, being older than 21 and those that prefer cheaper restaurants.
2. Coffee House coupons: In general, likelihood of accepting a coffee house coupon is 50%. Drivers that frequent coffee houses at least once a month or are below 21 tend to accept at higher rates.
3. Cheap Restaurant coupons: Acceptance rate of these coupons is fairly high at 71%. Drivers with a friend passenger, or that are driving in the afternoon, or are offered a coupon with expiration of 1d or work in sales & related field are likely to accept that coupon at an even higher rate of 80%+.
4. Expensive Restaurant coupons: These coupons have a low acceptance rate 44%. We were not able to identify attributes that might drive acceptance rate to 65%+ with a reasonable sample size.
5. Carry out & take away coupons: Acceptance rate of these coupons is high at 73% with some attributes scoring a rate of 80%+ including driving in the afternoon, working in Business and financial sector or having an associate degree. 
#### Limitations 
This is a multifactorial problem with numerous attributes and multiple values for each attribute. On one hand, to understand the contribution of multiple conditions simultaneously on likelihood of accepting coupons is challenging to accomplish in an exhaustive manner. On the other hand, exploring likelihood of accepting coupons based on one condition at a time (as was explored here) might miss out on indentifying dependent variables that up significantly the likelihood of acceptance when considered together. Algorithms that can systematically assess this multifactorial problem should be considered here for an exhaustive assessment.  
Furthermore, the cutoffs used in this analysis to identify attributes with high likelihood of acceptance (e.g. Pacceptance >= 65% for a sample >= 100 drivers) are subjectives and can be adapted. 


### Next Steps and Recommendations 
Consistently across the analysis, we found in general that drivers that frequent a certain place several times are more likely to accept the coupon offered for that place. Overall, cheap restaurant and carry out/takeaway coupons had a very high acceptance rate across various driver and driving attributes. If we are aiming to maximize coupon acceptance, we recommend considering these findings in customizing who is offered what and what types of coupons are offered. 

