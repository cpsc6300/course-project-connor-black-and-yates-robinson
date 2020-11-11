# TITLE: Predicting the MLB Home Run Leader
## Team Members: Connor Black, Yates Robinson
## Date: November 11, 2020

# Project Description
## Problem Statement and Motivation
This project aims to predict the Home Run Leader for the MLB in the next year according to previous years’ player statistics to have a better idea of which player will lead the league. Growing up playing baseball and watching the MLB has interested us since we were kids and wish to develop a closer understanding of player growth and predictions. These predictive models could potentially net us money based on selling this predictive solution to professional sports networks or betting companies.

## Introduction and Description of Data
Every year the Home Run Leader title is a hotly contested title as many of the best players in the league attempt to take the crown. Along with this a lot of people tend to bet on this statistic and predict who at the end of the season will have the most home runs. This problem is somewhat challenging as baseball is often very unpredictable and almost anyone having a hot season can take the title. Given this unpredictability it becomes hard to bet on a player and win. Showing recent trends among the previous home run leaders and other relevant stats will graphically display how the predictive model comes up with the player who is most likely to win.

Predictive models may be able to path an accurate set of players that put up big numbers in the coming seasons. Baseball Reference has data dating back to 1871 regarding the home run leader using the most accurate and up-to-date statistics. This gives a large statistical foundation to being able to come up with a model that can pull other stats from the past home run leaders and potentially create a trend to home run leaders in future seasons. There are a few player statistics that we feel are pertinent to our model such as league (LG), plager age (Age), total games played (G), plate appearances (PA), at-bats (AB), home runs (HR), strike-outs (SO), walks (base on balls or BB), batting average (BA), and slugging percentage (SLG). We feel these statistics are important to the player being evaluated when considering their performance at the plate. The factors stated are being tracked due to these reasons:
League (LG): There are discrepancies between the National League and American League when talking about home runs. It appears that the American League, traditionally, outperforms the National League hitters when it comes to hitting home runs (barring the years when the American League didn’t exist such as 1871-1881 and 1893-1900). This could be due to a number of factors such as better recruiting and scouting done by the American League or due to the way the differing and larger dimensions of National League ballparks deny players a home run ball compared to an American League park.
Player Age (Age): As with any player in any sport, performances can raise and decline as a player starts to add on years. When starting in the major leagues, a player could have worse stats than 5 years down the line when they have more experience under their belts. The same player could have worsening stats 10 years down the line due to physical limitations and body aging preventing the same performance at their body’s “natural peak”.
Total Games (G): The total number of games a player plays in over the course of a season is pertinent to understanding a high level aspect of the relative time they have a chance to hit home runs over the course of a 162 game regular season (not including post-season games).
Plate Appearances (PA): Plate appearances numbers the total times a player steps up to the plate. This statistic describes the number of chances each player has to hit a home run by stepping into the batter’s box.
At Bats (AB): At Bats are the total number of times a player has hit the ball into play (including a home run) and the number of times that player has gotten out. This can be considered an alternate approach to Plate Appearances if we need to dismiss walks (BB), hit-by-pitches (HBP), sacrifice fly outs (SF), and sacrifice hits (SH).
Home Runs (HR): This statistic simply speaks for itself when considering a model for the player who will have the most home runs in the coming season. Using previous years statistics, we can look at which players may be on the rise or fall of their professional careers in the home run category.
Strike-Outs (SO): We want to track this statistic as we feel striking out is a negative impact on a hitter’s ability to hit home runs. Striking out determines that a player is swinging at a ball and not hitting it or looking a ball go by them inside the strike zone when they have 2 strikes to begin with. Both of these circumstances add a negative weight to determining who has the highest potential in hitting the ball, let alone hitting home runs.
Walks (Base on Balls or BB): We want to track this statistic as we feel walking is indicative to being selective when hitting and being able to wait until the hitter gets a pitch they want to swing at. Being selective at the plate allows for the hitter to see more pitches and hone in on a good pitch to hit.
Batting Average (BA): Batting Average is the amount of hits a hitter gets in their total amount of at-bats. We will only use this as a comparison to a player’s Slugging Percentage which we feel is more indicative of a player’s ability to hit home runs.
Slugging Percentage (SLG): Slugging Percentage is an interesting statistic that we feel can bring a lot of power (pun intended) to the accuracy of our predictive model. Slugging Percentage is a better representation of batter productivity than batting average to our model since we are interested in home runs. Slugging Percentage is a scale of 0-4 that represents a hitter’s ability to get on base. If a hitter gets a single and reaches first base in 1 at-bat, they have a Slugging Percentage of 1.000. If a hitter gets a double/triple/home run and reaches each respective base in only 1 at-bat, they have a Slugging Percentage of 2.000/3.000/4.000. This statistic grants a higher weight to the more bases a player reaches due to their performance at the plate. The higher a player’s Slugging Percentage is, the more “power” they have at hitting the ball further and potentially hitting more home runs (this is overly simplified, however, we feel a great basis of understanding as to why this statistic is important to our model).

## Literature Review/Related Work 
- http://www.baseballdatascience.com/analyzing-the-mlbs-home-run-boom/
- https://www.baseball-reference.com/leaders/HR_leagues.shtml

For the most part, predicting the home run leader for each MLB season has been primarily untouched. This provides a relatively new and unexplored field for machine learning to present hidden trends and data that were previously unknown or heard of. Since the 2002 Oakland Athletics, statistics and sabermetrics have been a booming area of research in baseball. Machine learning will likely begin to utilize these new tracked pieces of data to predict games of baseball at a more accurate rate. There have been studies recently showing the explosion of the number of home runs hit each season since 2016. Those who follow the sport can only guess at where this spike in home runs came from; whether the ball is 'juiced' in the hitter's favor or whether the hitters themselves are 'juicing'. Whatever the explanation may be, there comes a question as to who the eventual season leader in the home run category will be.

## Interim Results
	 We currently feel our data points previously selected are a good starting point in creating a usable model to predict next season’s home run leader. Adding positive and negative weights to specific data is the most challenging for us to gauge as we don’t know the exact impact of the statistics we are analyzing. Stats like walks (BB) are confusing for us as a higher walk percentage should represent a good indicator of a player seeing the ball clearly and being selective at the plate (a positive weight), however, drawing a higher number of walks also reduces the chances the player gets at hitting home runs as their at-bats obviously result in a walk (a negative weight). Strike-outs are a heavily negative weight as they indicate a player isn’t seeing the ball well and they are reducing their chances of hitting home runs by being struck out. Finding these weights and supplementing our model correctly with them is the most difficult task we are currently experiencing.

# Project Progress
Our plan to accomplish this prediction is to find the current longest active player in the MLB and based on that we will grab all data (batting average, home runs, games played, etc.) from that point forward for all current players in the MLB. Along with this we will get data of all past home run title winners to create a baseline for stats of a home run title winner. With our current player data we will find the trend for each player and predict their stats in all for the 2021 MLB season. Using the baseline generated from past title winners, we will be able to see which players, based on prediction, have the best chance of winning the title in the 2021 season and how many home runs they will hit.
Meeting Times:
We plan to have roughly 1-2 2-hour work period(s) every week on Monday/Wednesday to achieve our goals.
Resources:
MongoDB
MkDocs
Viola


Milestones:
Website and Final Report (Dec 10, 2020)
Notebooks and Other Supporting Materials (Dec 10, 2020)
Team Evaluation (Dec 13, 2020)

# References:
We plan to retrieve data from:
https://www.mlb.com/ 
https://www.baseball-reference.com/ 
We plan to use:
https://www.mongodb.com/ 
http://palmetto.clemson.edu/ 
https://www.palmetto.clemson.edu/jhub/hub/ 
https://www.mkdocs.org/ 
https://voila.readthedocs.io/en/stable/ 
