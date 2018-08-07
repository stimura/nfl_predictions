# nfl_predictions

Can We Beat FiveThirtyEight's NFL Predictions Using Madden Individual Player Data?

This repository contains code and data to accompany three models: 
  1. The original FiveThirtyEight NFL Elo Model
  2. Random Forest Model of Madden 19's Individual Player Ratings 
  3. Logistic Regression of Madden 19's Individual Player Ratings
  
  
Model 1: FiveThirtyEight's NFL Elo Model

The Elo ranking algorithm was created by [Arpad Elo](https://en.wikipedia.org/wiki/Arpad_Elo), a Hungarian-American physics professor, to rank chess players in head to head matchups. FiveThirtyEight adopted the algorithm to build a ranking model for sports. The Elo model works especially well with zero sum games. In chess, just like in the NFL, only one player (team) can win and the outcome of each game impacts the relative ranking of the player (team). The rankings, derived from wins/losses in previous games, become part of the Elo model and is used to predict future wins/losses and the difference in ranking between two players (teams) becomes the greatest predictor of the winner/loser in head to head match up between the two players (teams). 
  
The data for our Elo model was derived from FiveThirtyEight's [historical NFL data](https://github.com/fivethirtyeight/nfl-elo-game/tree/master/data). We recreated this model and used the [2018-2019 NFL Schedule](https://www.pro-football-reference.com/years/2018/games.htm) to predict the 2019 Super Bowl Winner. 

Ultimately, this model became our control and we used it to informally calibrate our other models.


Model 2: Random Forest  and  Model 3: Logistic Regression 

We derived the data to train this model on ESPN's NFL Standings from [2012](http://www.espn.com/nfl/standings/_/season/2012) to [2017](http://www.espn.com/nfl/standings/_/season/2017) and [Madden Ratings](https://maddenratings.weebly.com/madden-nfl-19.html) for the corresponding year.   

Model 2: Random Forest

The Random Forest algorithm was great to model Madden Ratings data because there are between 54 and 66 unique variables for each individual player. Unlike the Elo model where each team is evaluated and ranked, Madden 


  
  
  
