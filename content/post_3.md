---
categories:
- Project
- PPUA5262
- BARI
- Spatial Analysis
date: "2021-12-10"
description: Analysis of food safety testing data reports for restaurants in Boston, USA
draft: false
tags:
- R-studio
- ggplot
- regression
- correlation
title: The evaluation of negative impact of violation on restaurants in Boston.
---

![cover](/blog/post_3_files/cover.webp)
# Executive Summary
The dataset describes the structures and organizations of the Food Establishment Inspection dataset gathered by the Boston Area Research Initiative (BARI). The Food Inspections dataset is including all food establishments in the City of Boston contains sanitary codes and standards.

By overlooking our data, our goal is to use the variables from the data to build a predict model or ranking system for restaurants based on different types of violation records.

# Main findings
•	Some neighborhoods have very low license active rate and violation pass rate, but they have a good taste of food based on the comments from the customers. 

• The longer duration of a restaurant's license has better violation test pass rate, we run correlation test and regression model that find out the duration of license and violation pass rate have very strong positive correlation. 

•	Violation scores and the vulnerability model for restaurants, we are using violation description to select keywords for the list and convert them into dummy variables, based on the dummy variables multiplied by different violation levels, it turns out our final violation score to evaluate the negative impact toward restaurants. 

•	Using Violation pass rate and license active rate to build restaurants operation rate:
it will give us three different results on each record (2,1,0), for the record has both pass on violation test and active on license status is equal 2, and violation test is pass and inactive on license status or get fail on violation test and active on license status is equal 1, and the records for both fail on violation test and inactive on license status.

![violation rate](/blog/post_3_files/project3-1.png)

# 1. Telling a data story

There are almost 300,000 records, and 31 variables in our data, the data collected from 2010 to 2020. We just focus on the violation level, violation status, license status. 

![violation level](/blog/post_3_files/project3-2.png)

# 2. Creating new variables

To better understand food inspection data, I select three major variables: city, license status, and violation status. The new variables that I created, violation pass rate, license active rate, and operation ability helped me find some fun facts about Boston’s restaurant. ![pass/fail](/blog/post_3_files/project3-3.png)
More than 65% of the restaurants have active license status. Then, more than 55% of restaurants have failed violations tests. Finally, only about 30% of restaurants have both passed the result on violation test and active license status.

# 3. Measuring new variables

I combine the violation status and license status, to calculate restaurants’ operation ability. Higher score means the restaurants have a good ability to handle and solve the violation issue in a short time or have those high standards of execution of a high standard of health safety environment.![pass rate](/blog/post_3_files/project3-4.png)![active rate](/blog/post_3_files/project3-5.png) Then using the license active rate and violation pass rate to make a model about restaurants’ quality. Based on violation status and license status as a measurement to evaluate the quality. Firstly, we used the new variables that transfer from the original variable ‘license status’: “active”, “inactive” as numeric, active=1, inactive=0, and another variable ‘violation status’: “Pass”, “Fail”, pass=1, fail=0. Second, we use new numeric variables: license status and violation status to calculate the mean in each city. The mean value in each city represents the percentage of restaurants that are being active or passing the test in that city. By observing the plots, the license active rate in each city looks similar, but the pattern in violation pass rate was different. There are some outliers in Chestnut Hill, and South End because there is only one restaurant on the record located in these two cities. 

![operation ability](/blog/post_3_files/project3-6.png)

Method: Operation ability = violation status (as. numeric) + license status (as. numeric)

# 4. Creating new violation scores 
Here is the chart after I aggregate the violation test pass rate (which from violation status), license active rate (license status), and violation score on city level. We are using those variables to work with our individual parts by combining our previous new variables. 

![table1](/blog/post_3_files/project3-7.png)

Using top 10 frequency word to generate my grading scale converting them into dummy variables, which including surface, Food, Floor, Walls/ceiling, Installation, Maintenance, clean, storage, facilities. Then, adding those 10 factors all together to create a "base score".

![table2](/blog/post_3_files/project3-13.jpg)

Function: Violation score= base score * violation level (1,2,3) *violation status (Fail =1, pass=0)

# 5. Observe the new variables on a Geographical level

![map1](/blog/post_3_files/project3-8.png)

By looking at the map, it is hard to find a clear pattern, but it can generally see some neighborhoods with low passing rate mostly located in Southern Boston, and most high passing rate neighborhoods are in downtown Boston and Northern Boston.

![map2](/blog/post_3_files/project3-9.png)

However, by observing the license active rate heat map was quite different from the passing rate map, in which the highest active rate was located at Southern Boston, and downtown Boston and Northern Boston had low license active rate.

![map3](/blog/post_3_files/project3-10.jpg)

Finally, looking at the violation score map, the distribution of the map is even, downtown Boston has a lower score compared to other areas, the restaurant located in the downtown area will have a better quality of restaurant compared to other areas.

# 7. Conclusion 
The violation score, and license active rate have negative correlation. Most restaurants usually got violation on level 1 with multiply times, we assume that when restaurant violations on level 1 which they didn’t pay much attention to it. We suggest that the Health Division of the Department of Inspectional Services should a system to calculate each restaurant’s violation status on a score level, when restaurant receive a violation with score, when the score reach recent point, license will be terminated. When the restaurant wants re-issue their license, they need serious test or pay fees to re-issue it.

[Back to Homepage](https://yizhen1106-portfolio.netlify.app/)