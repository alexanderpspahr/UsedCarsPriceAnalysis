# Analysis on Price of Used Cars

What drives the price of used cars? After running multiple models we can draw some conclusions about what factors most affect the price at which a used car will sell.

[Here](ModellingAndAnalysis.ipynb) is the in depth analysis and conclusions including source code for all models used and the entire process.

### Data
Data on used cars sourced from Kaggle. [Here](data/vehicles.csv)

### Methodology


### Goal
Deliver business actionable insights on the coffee house coupon group. What factors are highly correlated with accepting the coupon? What factors are correlated with rejecting the coupon?

# Insights
**Note: we will often refer to coffee house coupons as CH from this point forward.**

### Insight 1: Drivers who visit coffee houses more often are more likely to accept the coupon

![image](https://user-images.githubusercontent.com/129889030/230995133-af7d3638-1dfa-4a18-8d39-0f1ff9064c6e.png)

This may come as no surprise, but those who never visit CH are more likely to reject the coupon, while those who visit more often are more likely in general to accept. This remains true when controlled for other variables such as income, age, time of day, etc...

We can also clearly see that this trend is only for CH. It is not true that those who visit bars, restaraunts, or take-away are more likely to visit CH. Here is an example of 
what one of these graphs looks like:

![image](https://user-images.githubusercontent.com/129889030/230996220-619b0f8f-2691-412c-8f21-7564b14907f6.png)

As we can see there is no evidence of the same trend.

### Insight 2: Drivers who are alone are more likely to accept the CH coupon

When controlled for other variables. Drivers who are alone are more likely to accept the CH coupon

![image](https://user-images.githubusercontent.com/129889030/230997162-136e5798-f0dd-4a7f-a3cd-6b6d38fa4896.png)

When grouped by whether or not the driver had a passenger, they were more likely to accept if they were alone. The one standout passenger type is kid(s). In this case there is still a nearly 50/50 chance the driver will accept:

![image](https://user-images.githubusercontent.com/129889030/230997559-e9110054-bc4f-4635-9d02-58c8e6b5ddb4.png)

### Insight 3: Jobs have a notable effect on acceptance rate

Here is the acceptance rate of the CH coupon by occupation
![image](https://user-images.githubusercontent.com/129889030/230998018-f072ad5a-51f8-45e9-9210-d933de53b527.png)

Jobs classified as Healthcare Practitioners & Technical or Building & Grounds Cleaning & Maintenance were the two statistically significant examples of occupations which accepted more than average coupons. Building & Grounds Cleaning & Maintenance had a sample size of 11, however, so we can only say that Healthcare Practitioners & Technical are more likely to accept a CH coupon than any other occupation. With that being said, this is a potentially actionable item.

### Insight 4: People are less likely to accept CH coupons in snow

![image](https://user-images.githubusercontent.com/129889030/231000034-99ffd682-a137-433a-8d13-1c8d74709626.png)

I guess it is no surprise. We can surmise this likely applies to people who would intend to use the coupons immediately. Further study is needed on this item regarding the intensity of the snow, since snow is bad driving weather. We also need to do a study on whether the people that accepted or rejected the coupon in the snow planned to use the coupon now, or later.

### Insight 5: Above room temperature weather is correlated with CH coupon acceptance

![image](https://user-images.githubusercontent.com/129889030/231002515-5c60b5e8-16d4-457d-96df-c44ecb1ab22a.png)

Weather at ~80F has significantly greater proportion of CH coupon acceptances than weather below that threshold. This is a potentially surprising find given that one may assume that people enjoy drinking hot coffee during cold weather, but it is highly relevant.

# Conclusion - Business Actionable Items for the Future

**Here is a list of recommendations for groups to be targetted with extra CH coupons based on the findings in this report:**
1. People who frequent coffee houses
2. People who are driving in warmer weather (above room temp, approximately)
3. Healthcare and technical healthcare professionals
4. People who are driving alone

**Here is a list of items that require further study**
1. What criteria makes people who are driving with kids accept or reject the coupon?
2. How does extreme snowy weather compare with 'light' or 'average' snowy weather when it comes to coupon acceptance?
3. How do the groups which accept the coupon for immediate use vs groups who accept it for future use compare? Are there any differences?
