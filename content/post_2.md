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
Based on my living experience in Boston, it is hard to park on the street, most of the time street parking are always occupied.In this project, find some possible areas to install new parking meters based on current pattern of the parking meters’ distribution and relationship with land use map or correlate with other type of maps. 

# Research Questions:
1. What was the pattern of the parking meters? Based on different type of land use. Like residential vs. commercial.
2. Is there any relationship between population density among each block group?
3. Where are the places need to set up more parking meters?

# Data (Layers):
![Boston parking meter map](/./post_2_files/project2-1.PNG)

# Converted Layers:
  Central Boston: select Neighborhood blocks contains Parking meters.

![Central Boston](/blog/post_2_files/project2-3.PNG)

![Central Boston Clip](/blog/post_2_files/project2-4.PNG)
Central Boston Clip: using Central Boston layers to clip land use Boston.

# Methods
1. Select by attribute > Summary statistics > export feature
2. Using Clip tool to finalize appropriate size of map
3. Spatial Join tool
4. Using point density tool to create density heat map of parking meters

# Result & analysis:
1. Based on analysis the attribute table from parking meter layer, the distribution of parking meter near the land use type, it clear shows that most parking meters located near commercial area and residential area.![table1](/blog/post_2_files/project2-5.png)

2. The result for commercial and residential are most equally distribute. Then creating a density heat map for parking meters, which show an important finding in this project. The map shows that commercial area have higher density of parking meters. ![Parking meter density map](/blog/post_2_files/project2-6.PNG)
Looking at the clusters, the distribution of parking meters near commercial area were more clustered than    distribution of parking meters around residential area. It is better to set up more parking meters in commercial area. Also, by looking at commercial area, most clustered area has residential area next to it. The selection of place need meets the requirement at both commercial area and residential area.
![Parking meter density with land use map](/blog/post_2_files/project2-7.PNG)


3. Using 2010 population density map from Boston planning& development agency to compare my density heat map of parking meters. Visually, all the clustered places have a high population density except Downtown Boston. Based on the population density, the place with higher density has a higher demand of parking space.![2010 Boston population density map](/blog/post_2_files/project2-8.PNG)


4. Using 2021 median household income map as an indicator to determine whether the local government having more budget to set up parking meters. Higher median household income means local government getting more taxes, which have higher chance to spend money on parking meters.![2021 Boston Median Household income map](/blog/post_2_files/project2-9.PNG)



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



