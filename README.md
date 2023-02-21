# Soccer Player Value Project

## Project Description
Due to a common interest in soccer, we decided to examine the effect of different predictors on a player's market value. Tens of thousands of soccer players are transferred between clubs each year, and these players often cost clubs millions of dollars and play an integral part in team success. Because of this, the ability to identify undervalued or overvalued players is very desirable for club management. So, we looked at how predictors from the 2018-19 soccer season, such as total goals, total assists, minutes played, yellow cards, player position, nationality, age and height affected a player's market value (at the end of the 2018-19 season).


## Football Data From Transfermarkt Data Dictionary

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
