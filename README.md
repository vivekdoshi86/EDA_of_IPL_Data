# Exploratory data analysis of IPL data

## Introduction
Indian Premier League (IPL), Indian professional Twenty20 (T20) cricket league established in 2008. 
The league, which is based on a round-robin group and knockout format, has teams in major Indian cities.
The brainchild of the Board of Control for Cricket in India (BCCI), the IPL has developed into the most lucrative and most popular outlet for the game of cricket.
The eight founding franchises were the Mumbai Indians, the Chennai Super Kings, the Royal Challengers Bangalore, the Deccan Chargers (based in Hyderabad), the Delhi Daredevils, the Punjab XI Kings (Mohali), the Kolkata Knight Riders, and the Rajasthan Royals (Jaipur).
In late 2010 two franchises, Rajasthan and Punjab, were expelled from the league by the BCCI for breeches of ownership policy, but they were later reinstated in time for the 2011 tournament. 
Two new franchises, the Pune Warriors India and the Kochi Tuskers Kerala, joined the IPL for the 2011 tournament. 
The Kochi club played just one year before the BCCI terminated its contract. In 2013 the Deccan Chargers were replaced in the IPL by the Sunrisers Hyderabad.

## Problem Statement
IPL is the top level of the cricket league system.
It is contested by 8 to 10 teams, it operates on a system of promotion and relegation with the cricket League.
They have accumulated the data of all the matches that has happened betweeen 2008-2017 inclusively.
The company is trying to find the pattern of evolution of different teams over the years.
But their traditional systems are not up to the mark to find out deeper patterns.
To tackle this problem they hired me.

## Data Acquisition & Description
The dataset consists of information about all IPL matches from 2008 to 2017 with below details:

- Where it played (Venue & City), 
- IPL season
- name of teams who played against each other,
- When it played, 
- Who won the toss and what’s the decision of the Toss,
- Who won the match, by how many runs or wickets
- Who is the player of the match
- Name of both field umpires

## Data Description Observations
- We can see the description of only six continuous features – id , season, dl_applied, win_by_runs,  win_by_wickets, and umpire3.
- The id feature is an identifier so we won't be making any statistical observations for it.
- The season feature is an season year value so we won't be making any statistical observations for it.
- The dl_applied feature is a flag (0/1) stating whether Duckworth Lewis applied or not so we won't be making any statistical observations for it.
- The umpire3 feature is a third umpire name so we won't be making any statistical observations for it.
- Looking at the count value of the feature, we can see that data set is not having any value for umpire3.
- Looking at the values of the win_by_runs and win_by_wickets features, we can see that there is no negative value which implies that there are not having any misinformation.

## Data Information Observations
- There are 18 features with 636 observations.
- id, season, dl_applied, win_by_runs, win_by_wickets are of int64 data type.
- umpire3 is of float64 data type.
- All others are of object data types
- We will have to make more sense of Umpire3 by exploring them further.

## Data Pre-Profiling Observations
- There are 14 features with 636 observations in the dataset.
- 'city' feature has 7 missing values. 
- For one of the match 'umpire1' & 'umpire2' are having missing value.
- 'umpire3' feature has 100% of missing data.
- Dataset has No duplicate rows.
- 'date' feature seem to have unsupported data types.
- The dataset has No outliers.

## Data Pre-Processing
- Handled Missing values in city features by updating it with 'Dubai‘
- Reason updating it to Dubai is that all those 7 matches played on Dubai international cricket ground.
- Handled Missing values in Umpire1 & Umpire2 features – Have Googled the name of umpire for the match and updated the names accordingly.
- Handled missing values in Umpire3 by dropping the column itself.
- Converted date column type from object to datetime type.

## Data Post-Profiling Observations
- There are no missing values in the dataset.
- There are no duplicate values in the dataset.
- There are no outliers in the dataset.

## Exploratory Data Analysis
I have done EDA on below topics.
- Number of matches played in different cities
- Number of matches played in different grounds
- Number of matches played by each team
- Number of matches won by each team
- Number of matches played each year/season
- Winning toss really an advantage
- Proportion of Toss decisiion (bat/field)
- Top 10 Umpries most number of matches
- Top 10 Man of the match across all seasons
- Top 5 Man of the match each season
- Score closeness when team batting first
- Victories in numbers while chasing
- Home ground advantage

## Summary
Conclusion:
- Maximum number of matches palyed in Mumbai city, then Banglore, delhi and Kolkatta. But Chinnaswamy stadium is the ground wehere maximum number of matches played, then Eden gardens and Feroz Shah Kotla.
- Mumbai Indians has played maximum number of matches and most successful team compared to others.
- Winning toss gives a slight edge(51% probability of winning) against the opponents
- When chasing a target, the biggest victory was by 10 wickets(without losing any wickets) and there were 10 such instances. But Royal challenge Banglore is one team who has done twice.
- 57.1% of times, team had selected fielding first after winning toss.
- Chris Gayle has won the maximum number of player of the match title
- Six Indian players have figured in the top ten IPL players MOM winner's list.
- Dharmasena has officiated the most number of IPL matches on-field

Actionable insights:
- By analysing the data in this way, we can uncover different seasons matches that behave in similar ways.
- This level of matches segmentation is useful in analysing team overall performances.
- If we get ball by ball details of matches then I can anlayse individual player stats which can be useful to each team.





