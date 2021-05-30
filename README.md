# Pyber_Analysis
PyBer Project Folder
## Overview
### Purpose of Analysis
This project folder provides a summary analysis of the Pyber ride sharing datasets. For the challenge assignment, I constructed one summary dataframe and a chart that plots weekly data on fares for each city type. In the below sections, I will detail how the data looked and the steps I went through to provide my summary analysis. I will also compare the differences in ride-sharing data between each city type and provide three recommendations to PyBer for addressing disparities between these city types.
### Dataset
The original data consisted of two separate datasets, one with city-level information and one with ride-level information. The city dataset broke down the number of PyBer drivers and the city type (i.e., rural, suburban, or urban) for each city. See below for a sample of the dataset. 

![City Dataset](https://github.com/SethBoswell/PyBer_Analysis/blob/main/Resources/city_data.png)

The ride data contains information on each individual ride someone took using PyBer between January 1st, 2019 and May 8th, 2019. For each ride taken, the dataset tracks the timestamp when the ride was taken, the city in which the ride occured, the fare, and the ride identification number. See below for a sample of the dataset. 

![Ride Dataset](https://github.com/SethBoswell/PyBer_Analysis/blob/main/Resources/ride_data.png)

The first step of the analysis was to merge these two datasets so that I could include the city information with the ride dataset. To do this, I used the Panda's merge function 
on the city column between the two datasets to create the below table.

![Merged Dataset](https://github.com/SethBoswell/PyBer_Analysis/blob/main/Resources/merged_data.png)

## Results
### Summary Dataframe Resultss 
To construct the summary dataframe, I grouped the merged dataset by city type and calculated the following information:
- Total number of rides for each city type
- Total number of drivers for each city type
- Total amount of fares collected for each city type
- The average amount of fares collected per ride for each city type
- The average amount of fares collected per driver for each city type

Below I have included the summary dataframe.

![Summary Dataframe](https://github.com/SethBoswell/PyBer_Analysis/blob/main/Resources/PyBer_summary_dataframe.png)

As you can see, there is a strong, positive correlation between the amount of urbanization and peoples' use of PyBer's services. Urban cities have almost three times as many rides compared to suburban cities and thirteen times as many rides compared to rural cities! Furthermore, urban cities have nearly five times as many drivers compared to suburban ones and thirty times as many drivers compared to rural ones. Logically, it follows that the amount of fares collected by urban cities is twice as many as suburban ones and nine times as many as rural ones. 

The cost of using PyBer in rural areas is also more expensive. The summary dataframe shows that the average fare per ride in rural cities is $34.62 compared to $30.97 in suburban cities and $24.53 in urban cities. It is unclear whether the increase in fares is due to longer distances or higher rates in rural areas, although it is likely a combination of both. Finally, the average fare per driver is much higher in rural areas at $55.49, compared to $39.50 in suburban cities and $16.57 in urban cities. Higher per ride fares in rural cities combined with less drivers is the reeason behind these results.

### Mult-Line Plot Results
To construct the mult-line plot, I started by grouping the merged dataset by both city type and date. I then created a pivot table that lists the sum of fares for each city type on each date. I filtered the data to include only dates between January 1st and April 29th and then resampled the dataset to aggregate the dates into a weekly total. Below is the results of dataset where each point in the line charts represents a new week. 

![Summary Dataframe](https://github.com/SethBoswell/PyBer_Analysis/blob/main/Analysis/PyBer_fare_summary.png)

This chart reinforces the idea that rural cities collect far fewer fares on a weekly basis compared to suburban and urban cities. Throughout the entire period of time, the amount of urban fares collected was always about much higher than rural fares and suburban fares with suburban fares also being higher than rural. 

## Summary
Based on the above analysis, there are clear disparities between the different city types. Rural Pyber customers use the service less, pay more per ride, have less resources (drivers) available to them, and produce less revenue (fares) for Pyber. There are really two options available to Pyber: either they can prioritize their urban customers, who currently appear to be their most profitable customer type, or they can attempt to reduce the disparities between the rural customers and their suburban and urban counterparts. 

If the objective is to prioritize urban customers, I would recommend the following options:
- Continue to offer lower fares to urban/suburban customers and possibly provide discounts 
- Continue to add more resources such as drivers to urban/suburban areas while not offering the same level of service to rural customers.
- Add more promotions such as billboards and flyers in urban/suburban areas while spending little marketing efforts in rural areas

However, if Pyber management thought there was untapped potential in rural areas, they could attempt to alleviate the disparities between their customers and do the following:
- Equalize rates across the different customer segments or provide discounts to rural customers who pay have to longer trips 
- Add more drivers to rural areas to provide better service and lower wait times
- Starting advertising or promoting in rural areas to gain recognition and increase fares from rural customers.

The same holds true for suburban customers if management saw untapped potential with these customers. 


