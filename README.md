# DengAI: Predicting Dengue Fever Spread

This data project is about predicting disease spread using environmental data as well as historic numbers for reported cases in San Juan, Puerto Rico and Iquitos, Peru.

*Background:*

Dengue fever is a mosquito-borne disease that occurs in tropical and sub-tropical parts of the world. In mild cases, symptoms are similar to the flu: fever, rash, and muscle and joint pain. In severe cases, dengue fever can cause severe bleeding, low blood pressure, and even death.

Because it is carried by mosquitoes, the transmission dynamics of dengue are related to climate variables such as temperature and precipitation. Although the relationship to climate is complex, a growing number of scientists argue that climate change is likely to produce distributional shifts that will have significant public health implications worldwide.

In recent years dengue fever has been spreading. Historically, the disease has been most prevalent in Southeast Asia and the Pacific islands. These days many of the nearly half billion cases per year are occurring in Latin America.

Goal definition:

*The goal of the project is to predict the total_cases label for each (city, year, weekofyear) from the given test data set.*

## The Big Picture

A solution to this problem could help medical service providers in San Juan, Puerto Rico and Iquitos, Peru to handle the disease: reducing response time, providing vaccine in time, as well as antibiotics and the hospital capacity to treat the disease.

According to WHO, such methods are already employed for diseases that have epidemic potential:
http://www.who.int/globalchange/publications/oeh0401/en/index4.html

The problem should be addressed using offline supervised learning. Performance of the model will be evaluated by the mean absolute error to the actual # of reported cases.

*Assumptions:*

* climate data can be used to predict mosquito populations

*Evidence:*

"Research indicates that the daily mean temperature and the variation in temperature are two of the most important drivers of the current distribution and incidence of dengue. Precipitation and precipitation extremes, whether associated with drought or excess rainfall, also affect mosquito abundance and arbovirus incidence. Studies generally project that, as temperatures continue to rise and precipitation patterns change, opportunities are increasing for further geographical expansion of Aedes vectors and of dengue."

Ebi, K. L., & Nealon, J. (2016). Dengue in a changing climate. Environmental research, 151, 115-123.

## Modeling Results

I have achieved a mean absolute error (MAE) of 13.31 using Support Vector Regression. 

For comparison I also deployed a simple sequential neural network, which after some tweaking achieved a MAE of 13.17 - slightly outperforming SVR.

That means my prediction is only 13 reports off from actually reported cases!

Current leaderboard: https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/leaderboard/
