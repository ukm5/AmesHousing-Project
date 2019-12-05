# Project 2: Ames Housing Data 

## Problem statement: 

### How does adding a central air conditioning unit change the house saleprice?

## Executive summary

In this project, a simple linear regression model approach is taken to use the Ames housing data to understand what kind of houses tend to benefit from adding a central air conditioning unit. The data has been split into that for houses with and without air conditioning. For this study, only the basic features of a house have been considered, these features include bedrooms above ground, kitchen, full baths, and ground living area. In this work, it was noticed that it is not the size of the house but the number of rooms that contributes the most to whether adding a air conditioning unit is beneficial or not.

### Contents

- [Data cleaning performed in 01_EDA_and_Cleaning.ipynb](#Exploratory-Data-Analysis)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Model Development](#Linear-Regression-model-to-predict-price-of-house)
- [Data Visualization](#Visualize-the-data)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Data Dictionary

Data dictionary for the dataframes relevant to this project:

|Column Name|Type|Description|
|---|---|---|
|`saleprice`|float|Sale price of the house in dollars|
|`gr_liv_area`|float|Total ground living area|
|`bedroom_abvgr`|int|Bedrooms above the ground|
|`full_bath`|int|Number of full bathrooms|
|`kitchen_abvgr`|int|Number of kitchens above ground|
|`central_air`|object|{'Y', 'N'} : Houses with or without a central air conditioning unit|


All data obtained from the Ames housing project on [Kaggle](#https://www.kaggle.com/c/dsi-us-9-project-2-regression-challenge/submissions)

Detailed data dictionary for the entire data is available [here](#http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)

## Conclusions and Recommendations

For the data that we have obtained and analyzed, we have made the following inference and conclusions:

* We have fit a Linear Regression model that has a low variance and high bias, giving a r2 score of around 0.58
* We observe that adding a central air conditioning unit increases the saleprice of a property by 60% on average
* The houses that showed a decrease in saleprice, upon upgrading to a central air-conditioning, are the houses with more bedrooms (median number of rooms around 3.5, compared 2.5 of houses that increased in price)
* These houses, however, show lesser area per rooms, showing that it is not in the size of the room but the number of rooms which decides the increase or decrease in saleprice (difference of about 100 square units between the two kinds of houses)
* Houses of average saleprice lesser than 100,000 benefit more from adding a central air unit
* All the other parameters considered in this model seem to have minimal contribution to the end result as is evident from the almost similar statistics with respect to these parameters

From the analysis it is clear that adding a central air conditioning unit would be great idea to increase your saleprice (60% increase!), however, this is a better strategy for houses with 3 or lesser bedrooms.
