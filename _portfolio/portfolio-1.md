---
title: "Geospatial Explanatory Modeling of the U.S. Drug Overdose Epidemic"
excerpt: "<img src='/images/overdose_cover.png'><br/><br/>Short description of portfolio item number 2"
collection: portfolio
---

Check out this slide deck to get a quick overview of this project: 

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTwHy4oVQLOq2XaQOHJ0SuZl2qeyPU1jzc7YnCI00WnBplgJ_CMea61TNMmnvgpu4VOKltChKcWn-sP/embed?start=true&loop=true&delayms=7000" frameborder="0" width="700" height=auto allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTwHy4oVQLOq2XaQOHJ0SuZl2qeyPU1jzc7YnCI00WnBplgJ_CMea61TNMmnvgpu4VOKltChKcWn-sP/embed?start=true&loop=true&delayms=7000" frameborder="0" width="750" height="auto" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>



## I   Problem Description 
Throughout the years, there has been a dramatic increase in drug overdoses. We are currently at the point where overdoses are the cause of more deaths than car accidents, guns, or HIV. [1] Since 1999, there have been about 1 million fatal overdoses in the United States and just within the past year, over 100,000 have lost their lives due to overdose. [2] It is very clear that the drug epidemic is a widespread societal problem that needs to be properly researched and addressed. 
To do so, our team will be analyzing the number of fatal overdoses in United States counties throughout the last 20 years and exploring the question: Which characteristics of U.S. counties can best explain drug overdose rates? We also hope to estimate overdose rates in the counties that are missing data in our main overdose dataset. The successful completion of these tasks will allow us to provide policy makers with valuable information about the areas of the U.S. that are not easily observed simply with the raw overdose counts as well as insight as to what factors to focus on and which communities should be addressed more urgently when trying to counteract the drug overdose epidemic. 

## II   Data description 
Data Generation 
Our team obtained our drug overdose data from the CDC Wonder Search website by requesting data that specifically pertains to overdoses using their “underlying cause of death” codes. [3] The CDC collected this data through the Vital Statistics Cooperative to provide health departments and the general public with open access to detailed information that is beneficial in public health research and decision making. 

### Variables of Interest 
Our primary overdose dataset provides variables of interest such as year, county, overdose death count, and county population. We used these features to calculate the Overdose_Rate_per_100k which is the number of overdoses per 100,000 people. This will act as our main variable of interest. In this dataset, we observe a varying number of counties each year. However, the number of observed counties does increase throughout the years (Figure 1) and we have also confirmed that each year of data includes more than 50% of the United States population, despite missing a significant amount of counties. We have also gathered additional datasets detailing various factors that may relate to overdose rates (opioid dispensary rates [4], unemployment rates [5], ethnicity [6], poverty [7], median household incomes [7], jail populations [8], and other various health-related characteristics [9]). We have acquired all of our data by county and will be analyzing the relationships between our chosen features at this granular level. Unfortunately, we were unable to locate accurate and robust data for some of our additional variables on a county level before 2011. Hence, our analysis will focus on the years 2011 to 2020 in order to minimize the number of missing values while maintaining the wide time range of a decade. The final version of our dataset (Figure 2) includes 31,420 rows and 44 columns. 

### Hypothesized Relationships
Our team hypothesized that socioeconomic status would be closely connected to overdose rates. Hence, we included variables such as poverty and unemployment rates, assuming that overdose rates would be higher in counties where these factors were higher. We included median household income as well, presuming that counties with a lower median income would correspond with counties with higher overdose rates. We also surmised a possible association between higher opioid dispensary rates and higher overdose rates. Additionally, we explored the jail populations of each county, supposing that increased crime rates would correlate to higher drug use and therefore, a higher overdose rate. We considered the possibility that minority groups would be disproportionately affected by the epidemic and therefore, included each county's ethnicity and sex demographics as well. We also collected multiple features relating to health such as the percent of residents who are uninsured, are smokers, or are excessive drinkers, presuming that lower access to health care and higher rates of health complications would be related to higher overdose rates as well. Our team postulated that the urbanicity and total population of a county would be positively correlated with drug overdoses as well. Due to the clustering of higher overdose rates in different areas of the United States which can be seen in Figure 3, we hypothesized that the geographical location of each county and their relative positions with each other would also be a 



![od_Fig3](/images/od_Fig3.png)
    
Figure 3. Average Drug Overdoses per 100k People in the United States by County (2011 - 2020)

strong indicator of overdose rates. So for each county, we calculated the average overdose rate of its adjacent counties during that year - which we labeled `Spatial_Mean` - believing that higher overdose rates in neighboring counties would correspond to a higher overdose rate in the focal county.  
