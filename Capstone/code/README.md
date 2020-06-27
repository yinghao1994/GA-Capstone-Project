# Capstone Project: Fantasy Premier League
#### Don Chng, General Assembly SG-DSI-14
#### 28th June, 2020

## Problem Statement

The aim of this project would be to find out if it is possible to predict players who would perform well in the Fantasy Premier League from a machine-learning algorithm. We would want to build a machine-learning model to predict the a player's total points for the season based on the footballers stats with the lowest possible error. 

## Executive Summary

Both the train and test dataset had to be cleaned for numerous null values. Ordinal datatypes had to be switched into numbers and nominal datatypes encoded into dummy variables. 

Exploratory Data Analysis was first done to identify the relationships between the 80 variables. It was important to use a heatmap and correlation plots to identify correlations between the variables. 

An initial model was first created using linear regression, using variables that had high correlations to sale prices. In order to make sure that there was no stone left unturned, regularization models such as Ridge, Lasso and ElasticNet were used to comb through all the variables and minimize or eliminate those that are irrelevant. The aim was to identify which variables are most price sensitive, as well as to create a model that minimizes error.

## Conclusion

From the above models, we notice certain commonalities between key variables in models that have displayed a high sensitivity in prices, which are:
- Minutes
- Bonus Points System
- Goals Scored 
- Assists 
- Clean Sheet (Not letting in any goals)

To sum up, linear regression model has shown to be on par with models such as lasso and ridge regression models. Features such as minutes, goals and assists are still reliable predictors on how a player would do in future FPL Seasons. An important reason for this would be that most of the features are directly correlated to points obtained by a certain footballer. For example, if a player plays the full 90 minutes of the game, he would have more chances to score goals, create chances, getting clean sheets. Thus, the minute variable is the variable which has the largest coefficient. 
 

## Limitations

A major weakness of the model is that we do not take into account how the player performs over the season. 
There will be times where player form dips and we are not able to pick up on that. 
If given the appropriate data to model after subsequent gameweeks, we could use time-series modelling to account for the footballers playing matches week-in week-out. 

The models also do not take into account whether the player would be injured, or when they would have a dip in form and thus the manager would not select them. A player might do well for the first half of the season, but may be injured and there is no way of predicting when that will happen. 