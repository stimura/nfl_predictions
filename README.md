# nfl_predictions

Can We Beat FiveThirtyEight's NFL Predictions Using Madden Individual Player Data?

This repository contains code and data to accompany three models: 
  1. The original FiveThirtyEight NFL Elo Model
  2. Modification of Elo model using a new K
  3. Multiple models of Madden 19's Individual Player Ratings 

 
  
FiveThirtyEight's NFL Elo Model

The Elo ranking algorithm was created by [Arpad Elo](https://en.wikipedia.org/wiki/Arpad_Elo), a Hungarian-American physics professor, to rank chess players in head to head matchups. FiveThirtyEight adopted the algorithm to build a ranking model for sports. The Elo model works especially well with zero sum games. In chess, just like in the NFL, only one player (team) can win and the outcome of each game impacts the relative ranking of the player (team). The rankings, derived from wins/losses in previous games, become part of the Elo model and are used to predict future wins/losses and the difference in ranking between two players (teams) becomes the greatest predictor of the winner/loser in head to head match up between the two players (teams). 
  
The data for our Elo model was derived from FiveThirtyEight's [historical NFL data](https://github.com/fivethirtyeight/nfl-elo-game/tree/master/data). We recreated this model and used the [2018-2019 NFL Schedule](https://www.pro-football-reference.com/years/2018/games.htm) to predict the 2019 Super Bowl Winner. 

In this model, there are two "mysterious" parameters: the speed at which the model changes (k = 20) and home field advantage (home_adv = 65).

We made some modifications to K for our version of the model. 


To beat FiveThirtyEight, we tried lots of other models including: K-nearest Neighbors, Naive Bayes and Gaussian Bayes Classifier, Random Forest, Stochastic Gradient Descent, Perceptron, and Neural Networks. 

We derived the data to train this model from ESPN's NFL Standings from [2012-2013](http://www.espn.com/nfl/standings/_/season/2013) to [2017-2018](http://www.espn.com/nfl/standings/_/season/2018) and [Madden Ratings](https://maddenratings.weebly.com/madden-nfl-19.html) for the corresponding year. Unlike Elo, these models do not rely on head to head matchups. Therefore, the 2018-2019 season was not incorporated into these models. 

In the Madden Ratings data, there are between 54 and 66 unique variables for each individual player. Unlike the Elo model where each team is evaluated and ranked, we used the Random Forest model to search for the most important of the dozens of Madden variables to predict the best overall team based on the individual players. 








  
  
  
