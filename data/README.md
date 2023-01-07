# Data

If using an external dataset (that doesn't come in an R package), place data 
file(s) in this folder.

Then, include metadata about your dataset including information on provenance, 
codebook, etc.

The codebook for your data file(s) using the following format.

Data Description:

The original dataset used in our project is downloaded from the Kaggle webpage 
named "Football Data from Transfermarkt":
https://www.kaggle.com/datasets/davidcariboo/player-scores

The owner of this Kaggle project (username: DAVID CARIBOO) claimed that the 
dataset is scrapped and maintained using the transfermarkt-scraper to pull the 
data from Transfermark website and a set of Python scripts to curate it and 
publish it on the Kaggle website. The dataset is updated once a week (the 
version we used is from October 28th, 2022).

While the original dataset is composed of multiple CSV files with information 
on competitions, games, clubs, players and appearances. Each file contains the 
attributes of the entity and the IDs that can be used to join them together. 
Therefore, to ensure that we can conduct analysis based on as much information 
in the dataset, we joined the three datasets (players, player_valuations, 
appearances) and conducted initial data cleaning upfront to arrive at our 
dataset that will be used to produce analysis throughout our project. The 
cleaning includes dropping some repetitive or meaningless variables created 
through the join. Another thing note pointing out is that we filtered the 
dataset to only include the observations reporting the market value of player 
in the 2018-2019 season. This give us a consistent measurement of the variables 
without the need to counter the effect of againg and inflation. We named 
our cleaned dataset "transData". This dataset contains 13094 observations and 
27 variables. Our codebook will be based on the variables from this "transData"
dataset. 


## Name of data file

| Variable  | Description               |
|:----------|:--------------------------|
| player_id | id number identifying each unique player |
| last_season | the last season that the player made an appearance in a game |
| name | the player's name, format is all lower case with characters connected by "-" |
| pretty_name | the player's name, regular writing format with capital letters |
| country_of_birth | country name where the player was born |
| country_of_citizenship| country name where the player hold citizenship status |
| date of birth | the date on which the player was born, in "YYYY-MM-DD" |
| position | the position category at which the player plays |
| sub_position | the substitute position category at which the player plays |
| foot | the foot that a player use for soccer, categories include "Left", "Right", and "Both" |
| height_in_cm | the height of the player, in centimeters |
| highest_market_value_in_gbp | highest historical market value of the player posted on transfermarkt, in British Pound, as reported on transfermarkt website. Note, this historical value isn't necessarliy posted during the 2018-2019 season |
| agent_name | the name of the agent signed with the player |
| image_url | the link to a picture of the player |
| url | the link to the profile page of the player on transfermarkt website |
| club_id | the id number identifying each unique club |
| domestic_competition_id | identification of the domestic league at which the player plays at |
| club_name | the name of the soccer club the player serve, format is all lower case with characters connected by "-" |
| pretty_club_name | the name of the soccer club the player serve, regular writing format with capital letters |
| date | the date on which the "final_value" of the player is posted on transfermarkt website, in "YYYY-MM-DD". This is from the player_valuation dataset and comes in the same observation with the slice of the "final_value" of the player |
| dateweek | the date of the start of the week on which the "final_value" of the player is posted on transfermarkt website, in "YYYY-MM-DD". This is from the player_valuation dataset and comes in the same observation with the slice of the "final_value" of the player|
| final_value | the latest reported market value of the player during the 2018-2019 season, in British Pound, as reported on transfermarkt website. This variable is created by first filtering the joined data with only observations within teh 2018-2019 season, and slicing the dataset to only include the obersvations with the latest "date" for each player |
| total_goals | the total number of goals documented for the player during the 2018-2019 season. This variable is created by summing together the goals reported for each player in each distinct appearance from the "appearances" dataset, filtering based on only during the 2018-2019 season |
| total_assists | the total number of assists documented for the player during the 2018-2019 season. This variable is created by summing together the assists reported for each player in each distinct appearance from the "appearances" dataset, filtering based on only during the 2018-2019 season |
| total_minutes | the total number of minutes played documented for the player during the 2018-2019 season. This variable is created by summing together the minutes played reported for each player in each distinct appearance from the "appearances" dataset, filtering based on only during the 2018-2019 season |
| total_yellow | the total number of yellow cards given to the player during the 2018-2019 season. This variable is created by summing together the yellow cards given for each player in each distinct appearance from the "appearances" dataset, filtering based on only during the 2018-2019 season |
| total_red | the total number of red cards given to the player during the 2018-2019 season. This variable is created by summing together the red cards given for each player in each distinct appearance from the "appearances" dataset, filtering based on only during the 2018-2019 season |
