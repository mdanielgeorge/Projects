# Defeating West Nile Virus

## Team

Kaylin Tay
Daniel George
Teh Tze Yi

## Introduction

West Nile Virus (WNV) is a mosquito-borne zoonotic disease, that was first detected in the US during the summer of 1999 in New York City. WNV are primarily spread by a few Culex species, which can either contract the virus from infected birds or horses, or pass on the virus through biting the victim. The first human case of WNV was reported in Chicago in the year 2002, and since then have been steadily increasing.

## Problem Statement

The Chicago Deparment of Public Health and the city of Chicago have been working together since then to establish a surveillance system to monitor the number of mosquitoes that are found within the traps between spring and fall every year.

Given the data, we were then tasked to predict when and where mosquitoes will test positive for West Nile Virus and hence, effectively allocate resources towards preventing the transmission of west nile virus.

## Dataset

The three main datasets that were used in the Exploratory Data Analysis (EDA) and modeling were the main dataset that consists of: 

1.  A dataset containing location data for traps placed around Chicago to monitor mosquito populations. Samples from these traps were collected by city workers and tested for the presence of WNV.
2.  A dataset containing information about the weather occurring in the months when the mosquito data was being collected.
3.  A dataset indicating the dates and locations where pesticides were sprayed by the city to eliminate adult mosquitos.

Our goal was to perform analysis on the provided data and create machine learning models that predict the presence of West Nile Virus in mosquito samples. We used data from 2007, 2009, 2011, and 2013 to train the models; model performance was assessed using data collected in 2008, 2010, 2012, and 2014.

## Data Cleaning

Based on preliminary EDA, we found that WNV was only present within 2 specific species of mosquitoes - Culex pipiens and Culex restuans. As such, the remaining species were classifed under Culex sp. to minimise the noise from our modeling. There were also presence of missing data within the weather dataset, and they had to be dealt with by dropping them. There were also multiple duplicate points within the spray dataset and they were remove to ensure that the dataset is consistent throughout. Lastly, the main dataset was further classified into separate stations by using the respective latitudes of the northen-most airport (O'Hare International Airport) and the southern-most airport (Midway International Airport) and finding the center latitude between the two points. The datasets were then merged together for further analysis and modelling.

## EDA

1. Mosquito vectors
Only culex Restuans and cuplex pipiens have the virus. Other mosquitoes are not vectors for west nile virus.
2. Spraying
Spraying helps to reduce the number of mosquitos for about 10-15 days. 
3. Weather
Hot and humid weather are the best times for mosquitos to thrive. We see an increase in mosquitos during this period.

## Modelling

uggested Classification models 
- Logistics Regression
- GradientBoost
- AdaBoost
- RandomForest
Evaluation Metrics
- ROC-AUC Score
- F1 Score
- Recall

Summary Result

|Metrics|Logistics|GradientBoost|AdaBoost|RandomForest|
|---|---|---|---|---|
|AUC Train|0.83|0.92|0.89|0.86|
|AUC Test|0.76|0.84|0.83|0.82|
|Sensitivity|1.00|0.99|0.99|1.00|
|F1 Score|0.97|0.97|0.97|0.97|

Logistics Regression scored and performed the worst amongst the models and RandomForest gave us the best Results. However, when choosing our best model, GradientBoost is recommended for its ability to identify where the West Nile Virus is present.

## Conclusion & Recommendations

These are the locations which have a high count of mosquitos in Summer:
1. ORD Terminal 5, O'Hare International Airport
2. 4100 North Oak Park Avenue,
3. 1000 North Central Park Avenue
4. 7000 North Moselle Avenue
5. 3500 West 116th Street
We recommend spraying every 10-15 days in summer

