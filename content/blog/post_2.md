---

categories:
- Project
- PPUA5263
- Spatial Analysis
- Parking
date: "2022-05-01"
description: Boston street parking meter installation plan
draft: false
tags:
- ArcGIS
- QGIS
- R-studio
title: Boston street parking meter installation plan
author: Yizhen Zhang
---
![cover](/blog/post_2_files/cover.PNG)
# Introduction:
  Based on my living experience in Boston, it is hard to park on the street, most of the time street parking are always occupied, and I want use parking meter as my topic, and find some interesting information about it, to analyze the pattern of the parking meters’ distribution and relationship with land use map or correlate with other type of maps. 

# Research Questions:
1. What was the pattern of the parking meters (street parking)? based on different type of land use. Like residential vs. commercial.
2. Is there any relationship between population density among each block group?
3. Where are the places need to set up more parking meters?

# Data (Layers):
![Boston Parking meter shapefile](/blog/post_2_files/project2-1.PNG)
![Boston Neighborhood shapefile](/blog/post_2_files/project2-2.PNG)
# Converted Layers:
Central Boston: select by attribute table by Neighborhood names: Mission Hill, Longwood, North End, Roxbury, South End, Back Bay, Charlestown, West end, Beacon Hill, Downtown, Fenway, Brighton, South Boston Waterfront, Allston, and South Boston.

![Central Boston](/blog/post_2_files/project2-3.PNG)

Land use: remove Mixed Use, Industrial, ROW, Institutional land use, keep Residential, Commercial, and Public Open Space from symbology. 
Central Boston Clip: using Central Boston layers to clip land use Boston.

![Central Boston Clip](/blog/post_2_files/project2-4.PNG)
# Methods
1. Select by attribute > Summary statistics > export feature
2. Using Clip tool to finalize appropriate size of map
3. Spatial Join tool
4. Using point density tool to create density heat map of parking meters

# Result & analysis:
1. Based on analysis the attribute table from parking meter layer, I find out there are two major meter types which are single space parking and multiply space parking. Among multiply space parking meters, there are only 124 of 6955. However, the most multiply space parking meters were located at commercial area, which give my important findings. 
After I use space join tool, to figure out the distribution of parking meter based on land use. It turns out a table like below:

![table1](/blog/post_2_files/project2-5.png)

2. We can see the result for commercial and residential are most equally distribute. It is hard to tell any important relationships based on this table. Then I create a density heat map for parking meters, which show an important finding about this topic. The map show that the higher density of parking meters is located at commercial areas. The cluster at downtown Boston, Back Bay/Beacon Hill, Fenway/Kenmore, South End, and Allston. Based on this pattern, the distribution of parking meters near commercial area were more clustered and the distribution of parking meters around residential area were dispersed. I decided to set up more parking meters in commercial area. Also, by looking at commercial area, most clustered area has residential area next to it. The selection of place need meets the requirement at both commercial area and residential area.

![Parking meter density map](/blog/post_2_files/project2-6.PNG)
![Parking meter density with land use map](/blog/post_2_files/project2-7.PNG)

3. Using 2010 population density map from Boston planning& development agency to compare my density heat map of parking meters. Visually, all the clustered places have a high population density except Downtown Boston. Based on the population density, the place with higher density has a higher demand of parking space, and in this case, South Boston, North End, Allston, and Charlestown.

![2010 Boston population density map](/blog/post_2_files/project2-8.PNG)

4. Using 2021 median household income map as an indicator to determine whether the local government having more budget to set up parking meters. Higher median household income means local government getting more taxes, which have higher chance to spend money on parking meters. I select the region with above average median household income (City of Boston). Allston/Brighton, South Boston, Downtown, and Charlestown will be fitted area. 

![2021 Boston Median Household income map](/blog/post_2_files/project2-9.PNG)

# Limitation:
1. lacking data for parking meter around southern Boston area. 

2. Need an update version of population density map, 2010 was outdated. 

3. Need extra information on median household income around South Boston area, North End, and Charlestown.

# Conclusion:
Based on my several conditions about set up parking meters:
1. Must be Commercial area and there is a residential area near next to it.

2. High population density. 

3. The median household income in that area must greater than average median household income in City of Boston.

# Final Result:
![Final result](/blog/post_2_files/project2-10.PNG)

# Next steps:
Having updated maps (population density & income), having extra layers about the type of roads to determine which kind of road (street) allow to set up parking meters, and build a suitability model for parking meters.
For suitability model, I need several parameters in this model to rank the area with scores, have a better score means the area are more likely to set up parking meters.
Here is an example for possible parameter:
1. Distance to nearest residential area (3mile radius)

2. Road type (street is a best option)

3.	Population density block size (need greater than average density in city of Boston)

4.	Median household income block size (need greater than average level of city of Boston)

5.	Like people’s mobility on each block 

