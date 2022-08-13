---
categories:
- Project
- poster
- Visualization
date: "2021-01-01"
description: Visualizations for this entire Urban Informatics program
draft: false
tag:
- ArcGIS
- QGIS
- R-studio
title: My City Space and Time-Airbnb Dataset
---


![airbnb](/blog/post_4_files/airbnb1.webp)

In my Airbnb dataset, the data collected since 2019-01-17 to 2021-01-03, which was total 102 weeks. Based on that, I want to look at different room type for Airbnb. 
!
[airbnb_time](/blog/post_4_files/airbnb2.png)

Then, I used {sf} and {ggplot2} packages to make a spatial map. And trying to find some interesting information from the map.
![airbnb_map](/blog/post_4_files/airbnb3.png)

This map is about the distribution of each Airbnb based on different room type to see is there any a pattern about this map and any cluster for the room types.

In this map I wanted to see how landowner’ investment about their properties, so based on the map we can tell that majority of landlords have around 3-6 years of experience, it turns out that landlords with more experience tend to invest their money further away from downtown Boston, and there are far fewer landlords with 8+years of experience (darkest blue) than those with less than 8 years (white). 

![airbnb_landlord](/blog/post_4_files/airbnb4.png)

As a result, the colors on the map are bound to be lighter. Another reason may be that experienced landlords do prefer to invest outside of downtown Boston, as they prefer whole houses to apartments. Based on my last map, the majority of private rooms are locate at southern Boston, which is consider as moving their investment toward south. Although whole plumbing and apartments are grouped together in this dataset, in general, houses downtown are relatively small and those away from downtown are usually more spacious.

[Back to Homepage](https://yizhen1106-portfolio.netlify.app/)