layout: page
title: "NBA Data"
permalink: /maniar9.github.io/neilmaniar.github.io/nbadata

The NBA has grown a lot since its creation in 1946 including the addition of new rules, new teams, and the use of advanced analytics. The goal of my data exploration is to understand how the changes have impacted the league and the players. I take a look at 4 data sets from 1950 – 2022 for player salaries, player career stats, player box scores, and team payrolls. 
First I explored the datasets using the Python Pandas library, exploring and cleaning the datasets gives us a good idea of what we are looking at. Taking a look at the box_score table :
 
 ![image](https://github.com/nmaniar9/neilmaniar.github.io/assets/44175458/7e7bb0ad-bf65-4d95-94d7-7c4ce491a9d6)

 
We can see what data types are available in the data set with .info() and we can take a quick look at what the data looks like with .head(). We notice that some of the fields have NaN values, in this specific case it would make sense to fill the NaN values with zeros using .fillna(0) because we are looking at player statistics we can assume that some of the fields were not tracked before certain periods or they were missed. We should be aware that we are adding zeros when we begin the analysis. I also check for duplicate values in the data tables using .duplciated(). I run similar checks on the other 3 data tables and fix issues that occurred, the full file can be found in my .ipynb file on github.
One of the biggest changes in the NBA includes the addition of the 3-point line in 1979. So a big question is how has the 3 point line affected the game? 
Taking a look at how many 3 pointer were made during each season using the .groupby() function
 
We can see that the number of three pointers have increased consistently each season with some drops. Taking a look at other stats during the same time period we also see similar increases with similar drop offs. The 1999 and 2012 seasons were shortened from a lockout due to salary negotiations, the 2020 season was also cut short due to the COVID-19 pandemic. Can the 3 point shot be the main contributor to the total point increase? The NBA added many teams over the last 50 years with the last team being added in 2002, so it may not be realistic to only look at the number of FG (naturally more teams leads to more FG). If we take a look at the % of shots taken we can get a better understanding.
 
If we look at the shot selections over the last 50 years we can see that approximately 30% of shots taken are 3 pointers. 3 pointers are one of the major factors contributing to the point increase along with new teams, and slightly longer seasons.

Next lets take a look at the player level and how the league has changed for athletes. One of the biggest changes that can be seen in the salary increases. Looking at the total payroll (inflation adjusted) per season: 
 
The overall salaries have gone from 250 million to over 4 billion in the last 30 years. There are athletes in the NBA who have long term contracts worth more than total salaries of the 1990s. In the time period TV and broadcasting deals have contributed to the significant rise in pay.
To look at individual players I built a Tableau Public dashboard that allows you to look at career highlights as well as how that player stacks up in comparison to other players.
 
