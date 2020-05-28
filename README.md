# NBA Player Predictions
Predict the future of NBA players' careers. Full project published on [Towards Data Science](https://towardsdatascience.com/the-nbas-2023-mvp-is-ff78deb85122).

The general concept for this project is that a player's past performance and age are predictive of their future performance. Barring injury, a player's next season will usually be similar to their most recent season. With this in mind, it's possible to use statistics of past seasons to predict 1 season into the future. The output prediction can then be used as an input to predict 2 seasons into the future, which can then be used to predict 3 seasons into the future, etc. The model created in this project predicts the following 14 features: minutes played, two point percentage, two point attempts, three point percentage, three point attempts, free throw percentage, free throw attempts, defensive rebounds, offensive rebounds, assists, steals, blocks, turnovers, and personal fouls. Counting stats are predicted per 36 minutes then combined with predictions of minutes played to generate predictions of per game averages.

The repository contains 4 ipython notebook files.

1. CollectPlayerData.ipynb: Uses the Sports Reference API to build datasets of NBA player statistics at the season and career levels. These datasets are then saved in the Data folder as .csv files where they can be accessed by the other notebook files. This is the first notebook to run in order to reproduce the NBA player prediction model.
2. PlayerDevelopmentAnalysis.ipynb: Not necessary for reproducing the NBA player predictions. Instead this notebook uses the NBA player datasets to run an analysis of NBA player development. The analysis shows that players' tend to improve statistically up until the age of 25 then decline beyond the age of 28. It's also shown that players who enter the league at a young age generally have a longer period of development before reaching their statistical peak, and their statistical peak is generally greater than players who are older upon entering the league.
3. PlayerDevelopmentPredictions.ipynb: Uses the NBA player datasets to construct and train a recurrent linear regression model for predicting NBA player careers. The notebook engineers features, compares a few types of basic models, builds and trains a recurrent linear regression model, characterizes performance, then saves the final model to the Models folder. The notebook also contains a function for saving the results of performance characterization to the Results_Log folder. This is useful for comparing performance across various model iterations.
4. FuturePredictions.ipynb: Loads the NBA player datasets and prediction models, then uses these to predict player statistics for future seasons.
