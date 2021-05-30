+thater_Analysis
PyBer Project Folder
## Overview
### Purpose of Analysis
This project folder provides a summary analysis of the Pyber ride sharing datasets. For the challenge assignment, I constructed one summary datagrame aaa aaf chart that plots weekly data on fares for each city type. In the below sections, I will detail how the dataset looked and the steps I went through to provide my summary analysis. 
### Dataset
The original data consisted of two separate datasets, one with city-level information and one with ride-level information. The city dataset broke down the number of PyBer drivers and the city type (i.e., rural, suburban, or urban) for each city. See below for a sample of the dataset. 

The ride data contains information on each individual ride someone took using PyBer between January 1st, 2019 and May 8th, 2019. For each ride taken, the dataset tracks the timestamp when the ride was taken, the city in which the ride occured, the fare, and the ride identification number. See below for a sample of the dataset. 

The first step of the analysis was to merge these two datasets so that I could include the city information with the ride dataset. To do this, I used the Panda's merge function on the city column between the two datasets to create the below table
