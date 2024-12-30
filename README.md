# IPL Winner and Score Prediction
## Overview
This repository contains machine learning models designed to predict the score of the first inning and the winner of an IPL match. The dataset includes ball-by-ball information and match-level details for IPL Seasons 1 to 10 (2008-2017).

## Features
### Score Prediction
- **Ball-by-Ball Data**: Includes comprehensive details such as match ID, date, venue, batting and bowling teams, batsman, bowler, runs, wickets, overs, runs and wickets in the last 5 overs, and total score.
- **Regression Model**: Utilizes a regression approach to predict the score given the batting and bowling teams, current overs, runs, wickets, and performance in the last 5 overs.

### Winner Prediction
- **Match-Level Data**: Includes information such as match ID, city, date, player of the match, venue, teams, toss details, match winner, and result margin.
- **Classification Techniques**: Various classification models are employed to predict the winner of the match based on pre-match and in-match data.

## Dataset
### Ball-by-Ball Data
- `mid`: Match ID
- `date`: Date of the match
- `venue`: Venue of the match
- `batting_team`: Batting team
- `bowling_team`: Bowling team
- `batsman`: Batsman
- `bowler`: Bowler
- `runs`: Runs scored on the ball
- `wickets`: Wickets fallen
- `overs`: Current over
- `runs_last_5`: Runs scored in the last 5 overs
- `wickets_last_5`: Wickets fallen in the last 5 overs
- `striker`: Current batsman on strike
- `non-striker`: Current batsman on non-strike
- `total`: Total runs scored in the inning

### Match-Level Data
- `id`: Match ID
- `city`: City where the match was played
- `date`: Date of the match
- `player_of_match`: Player of the match
- `venue`: Venue of the match
- `neutral_venue`: Neutral venue indicator
- `team1`: First team
- `team2`: Second team
- `toss_winner`: Team that won the toss
- `toss_decision`: Toss decision (bat/field)
- `winner`: Match winner
- `result`: Result type (runs/wickets)
- `result_margin`: Margin of victory
- `eliminator`: Eliminator match indicator
- `method`: Method used if match was interrupted
- `umpire1`: First umpire
- `umpire2`: Second umpire

## Machine Learning Models
### Score Prediction
- **Regression Models**: Utilizes linear regression, decision trees, Neural Networks and other regression techniques to predict the first inning score.

### Winner Prediction
- **Classification Models**: Implements logistic regression, decision trees, random forests, Neural Networks and other classification techniques to predict the match winner.

## Data Analysis
- **Exploratory Data Analysis (EDA)**: In-depth analysis of the dataset to uncover patterns, trends, and insights.

## Example Usage
### Score Prediction
```python
batting_team = 'Chennai Super Kings'
bowling_team = 'Delhi Capitals'
score = predict_score(batting_team, bowling_team, overs=12.6, runs=101, wickets=3, runs_last_5=54, wickets_last_5=1)
print(f'Predicted Score: {score} || Actual Score: 171')
