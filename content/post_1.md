---
categories:
- Project
- PPUA6966
- Wildfire
- Air Quality
author: Yizhen Zhang
date: "2022-08-20"
description: 123
draft: false
tags:
- R-studio
- ArcGIS
- markdown
title: Data Analysis Report on the Relationship between Air Quality and Population Mobility in California, USA
---
![cover_fire](/./post_1_files/1280px-Bobcat_Fire,_Los_Angeles,_San_Gabriel_Mountains.jpg)

#Introduction
Based on unusual drought and heat exacerbated by climate change, in California overgrown forests caused by decades of fire suppression, and rapid population growth along the edges of forests. Wildfires increase air pollution in surrounding areas and can affect regional air quality. The effects of smoke from wildfires can range from eye and respiratory diseases. Children, pregnant women, and the elderly are especially vulnerable to smoke exposure. Emissions from wildfires are known to cause increased visits to hospitals and clinics by those exposed to smoke. 

![time serious wildfire](/./post_1_files/wildfire1.png)

The 2020 wildfire season has some of the most severe wildfires in years, raising pollution levels well above typical local ranges. Cities from Los Angeles to San Francisco have many days of air quality levels. Breathing air pollution can be deadly, and higher levels of air pollution increase the risk of adverse health effects. 
In this project, collecting PM2.5 concentration and AQI (Air Quality Index) value data from California for the year 2020, use R for data clarity, and generate visual reports to filter out the high concentration values and combine them with data from the California government to detect wildfires. Then, using ArcGIS to conduct a spatial analysis to compare the high PM2.5 concentrations in some areas with the current population mobility and to analyze whether there is a correlation. Developing a regression model, and it predicted that there will be a negative correlation between population mobility and PM2.5 concentrations when the wildfire happened.

#Air Data:
![air quality](/./post_1_files/wildfire3.png)
As the graph shows, the higher air quality values are concentrated in the months of July to October, while wildfires were frequent from July to October in 2020, with a total of 258 fires in the year according to government wildfire data, and 153 wildfires from July to October. It is observed that 60% of the fires in the year are concentrated in summer, and the high concentration of PM2.5 and the frequent occurrence of wildfires in this period, and it is concluded that there is a direct relationship between fires and air quality. Then further confirmation of the impact of wildfire on air quality is needed to confirm the reliability of the data through the population mobility.	

According to the Air Quality Index, the values greater than 100 were selected for focused analysis.
![AQI ](/./post_1_files/wildfire4.png)

# Wildfire Data

![wildfire](/./post_1_files/wildfire—CA.PNG)
The wildfire data came from the California Department of Forestry and Fire Protection, which used ArcGIS to select the incidents with wildfires burning area greater than 5,000 Ares. 

# Method:
Buffer: Use buffer tool to apply a 10-mile radius buffer for each air monitoring station. 
![buffer_10mile](/./post_1_files/buffer_10mile.PNG)

Remove overlap: When the buffer is created, there are some air monitoring stations with overlapping buffer, use the remove overlap tool to distribute the overlapping parts equally by using center line method.
![centerline_buffer](/./post_1_files/CL_remove_overlap_10mile_buffer.PNG)

Spatial joint: use spatial joint to select buffer and covered block group to calculate total mobility, using within and intersect method. (Left: within, right: intersect)
![within&intersect](/./post_1_files/within_intersect.png)

# Fire case 1: El Dorado
![ElDorado map](/./post_1_files/ELDORADO.PNG)

Start date: 09/05/2020

End date:   11/16/2020

Burned arc: 22744

City: Riverside

Mobility & AQI:
![el dorado-result](/./post_1_files/EL-Dorado-result.png)

# Fire case 2: Valley
![valley](/./post_1_files/VALLEY.PNG)

Start date: 09/05/2020

End date:   09/24/2020

Burned arc: 16930

City: San Diego

Mobility & AQI:
![valley-result](/./post_1_files/Valley-result.png)

# Fire case 3: SCU Lightning Complex
![CZU-fire](/./post_1_files/SCU_CZU_fire.png)

Start Date: 08/18/2020 

End Date:   10/01/2020

Burned Arc: 396624

City: San Clara

Mobility & AQI:
![scu-result](/./post_1_files/SCU_weekday_result.png)

# Fire case 4: CZU Lightning Complex

![CZU-fire](/./post_1_files/SCU_CZU_fire.png)

Start Date: 08/16/2020 

End Date:   09/22/2020

Burned Arc: 86509

City: San Jose, San Mateo, San Cruz

Mobility & AQI: 
![czu-result](/./post_1_files/CZU_weekday_result.png)

# Conclusion:
Based on the four cases mentioned above, it is possible to prove the initial hypothesis. When a wildfire occurs, it makes the air quality worse thus leading to a decrease in population mobility, and there is a negative correlation and regression in their relationship. By comparing the wildfire incidents that did not qualify. population mobility in its surrounding cities, it was found that the most important reason was the population density of the city, with higher population density being more susceptible. There are also cities where the pattern of population mobility decreases in the incident of a wildfire, but where the air quality index is under 100 during this period. All in all, this project finds the main research subjects, and the final results are predicted by further analysis and new models that enable local residents to have a better and safer life in the city, which can avoid unnecessary risks when people travel.



[Back to Homepage](https://yizhen1106-portfolio.netlify.app/)