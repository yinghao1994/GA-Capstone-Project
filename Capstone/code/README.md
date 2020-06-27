# Capstone Project: Fantasy Premier League
#### Don Chng, General Assembly SG-DSI-14
#### 28th June, 2020

## Executive Summary
Fantasy Premier League (FPL) is a fantasy sport management game; the aim being to score as many fantasy points as possible at the end of the football season. The results will be tabulated and the top scoring players will stand to win several attractive prizes.

A season consists of 38 gameweeks. At the beginning, fantasy players are given a virtual currency budget of $100 million. During each gameweek, players will have to pick a total of 15 footballers from the pool that is available in the Premier League. The draft consists of 2 Goalkeepers, 5 Defenders, 5 Midfielders and 3 Forwards. At any given gameweek, only 11 are allowed to be fielded (1 GK, 3-5 Defenders, 3-5 Midfielders, 1-3 Forwards) and 4 benched.

After the matches are played for each week, points are awarded based on how the statistics they have racked up in the match. Points can be awarded for minutes played, goals, assists, influence on the pitch etc. The default strategy of FPL is to pick good footballer that have the potential to rack up as many points as possible. However, it is also important that the fantasy players choose their footballers wisely as they have a limited budget.

## Problem Statement

The aim of this project would be to find out if it is possible to predict players who would perform well in the Fantasy Premier League from a machine-learning algorithm. We would want to build a machine-learning model to predict the a player's total points for the season based on the footballers stats with the lowest possible error. 

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
