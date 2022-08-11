---
categories:
- Project
- plots
- Visualization
date: "2021-01-01"
description: Visualizations for this entire Urban Informatics program
draft: false
tags:
- R-studio
- ggplot
- ArcGIS
title: Visualizations for this Urban Informatics program
---


![airbnb](/blog/post_4_files/airbnb1.webp)
# My City Space and Time Airbnb Dataset

In my Airbnb dataset, the data collected since 2019-01-17 to 2021-01-03, which was total 102 weeks. Based on that, I want to look at different room type for Airbnb. 
!
[airbnb_time](/blog/post_4_files/airbnb2.png)

Then, I used {sf} and {ggplot2} packages to make a spatial map. And trying to find some interesting information from the map.
![airbnb_map](/blog/post_4_files/airbnb3.png)

This map is about the distribution of each Airbnb based on different room type to see is there any a pattern about this map and any cluster for the room types.

In this map I wanted to see how landowner’ investment about their properties, so based on the map we can tell that majority of landlords have around 3-6 years of experience, it turns out that landlords with more experience tend to invest their money further away from downtown Boston, and there are far fewer landlords with 8+years of experience (darkest blue) than those with less than 8 years (white). 

![airbnb_landlord](/blog/post_4_files/airbnb4.png)

As a result, the colors on the map are bound to be lighter. Another reason may be that experienced landlords do prefer to invest outside of downtown Boston, as they prefer whole houses to apartments. Based on my last map, the majority of private rooms are locate at southern Boston, which is consider as moving their investment toward south. Although whole plumbing and apartments are grouped together in this dataset, in general, houses downtown are relatively small and those away from downtown are usually more spacious.


# Building Permit in Boston during COVID-19, and City's Development Trend

Research Question 1: How does COVID pandemic affect about Building permits, what is the trend for Building permit from 2006 to 2021?

![line1](/blog/post_4_files/building_permit1.png)

I created a line graph for 2010-2020 see- ing the number of building permits per year peaking before the COVID-19 pan- demic in 2019. In 2010, I also saw the market and economy still suffering from the financial crisis in 2008-2009.
Prior to the COVID-19 pandemic, annual permits appear to have peaked in 2019. As mentioned earlier, the decade 2010- 2020 was surrounded by a financial crisis and a global pandemic, so it should be expected that the urban cycle of redevel- opment experienced a natural increase in the years between these two events. It will be interesting to see if the sharp de- cline in building permits initiated in 2020 will rebound at the same level in 2021.

Research Question 2: How does the Building permit distribution in Boston area, which area has most Building permit and what is the building types of each permit, what is the Boston’s construction development plan?

![bar2](/blog/post_4_files/Building_permit2.png)

Finally, the top10 neighborhoods isolated, the types of land use that comprises each area and how they are unique and similar. It can clearly see majority of development is occurring in Downtown. It also notice that most neighborhoods in this redevelopment cycle are dominated by com- mercial and multi family (7+) development. This could perhaps be a good indicator of neighborhood mainly focus redevelopment on those fields.


Research Question 3: What is the difference between construction’s added values and its existing values, which types of properties were seeing the most improvement in value in redevelopment? What is the future development plan for city of Boston?

![map3](/blog/post_4_files/building_permit3.png)

Based on the maps, it can clearly see the building added values vs total values ratio the South Boston has higher ratio when it excluded Logan airport. It means South Boston having more investment compared to North Boston. By looking at the average age of building in each neighborhood, the Buildings located at the South Boston were older than North Boston. As I combined those map, the government sent more money on redeveloping the city. Like the plot from question 1, there is a rapidly growth in 2009 to 2010 which I assume that in 2022 there will be a rapid growth on Building permit, and especially concentrate on South Boston’s development, which can equalize the resource and economy among entire Boston city.

![NewYork](/blog/post_4_files/NYC1.png)
# The effect of COVID on NYC citizens by income (Year: 2020)

NYC has a vast income disparity by borough. The Bronx has one of the largest populations in NYC, second to Queens, but it contains the least amount of wealth (in comparison to population size). Brooklyn is composed of a population that has varied income, but most of the population makes less than $50,000 or are unemployed. Manhattan is the 3rd largest borough in terms of population, and the majority make over $50,000. Queens is the largest borough and has a mixed income population, with the majority making under $50,000 and a high unemployment rate.

![chart](/blog/post_4_files/NYC2.png)

COVID has very much effected NYC on an income level, impacting Brooklyn, Queens, and the Bronx. The line graphs to the left depict the cases infection cases, hospitalizations, and deaths (A, B, and C) over time. 

![line graph](/blog/post_4_files/NYC3.png)

Peak COVID infection occurred in Aril, the min and max for this time period are labeled for graphs A, B, and C. Queens has the highest COVID cases, hospitalizations, and deaths, while Staten Island had the lowest. This makes sense since Queens had the largest population and Staten Island the smallest. In terms of population size Manhattan is larger than Brooklyn; however, Brooklyn had the second highest COVID cases, hospitalizations, and deaths, while Manhattan had the second lowest. The difference between Brooklyn and Manhattan COVID cases, hospitalizations, and deaths is vast.

![line graph2](/blog/post_4_files/NYC4.png)

Vaccinations seem to be evenly distributed between all the boroughs, where vaccinations are most dense in areas where there is public transportation and hospitals.