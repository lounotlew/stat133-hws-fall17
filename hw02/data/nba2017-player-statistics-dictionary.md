---
title: "HW02: Data Dictionary"
subtitle: "Stat 133, Fall 2017"
author: "Woo Sik (Lewis) Kim"
output: github_document
---

**Source of Data**

http://www.basketball-reference.com

**Base column names and variables used in nba2017-player-statistics.csv:**

• Player: first and last names of player

• Team: 3-letter team abbreviation

• Position: player’s position

• Experience: years of experience in NBA (a value of R means rookie) • Salary: player salary in dollars

• Rank: Rank of player in his team

• Age: Age of Player at the start of February 1st of that season. • GP: Games Played furing regular season

• GS: Games Started

• MIN: Minutes Played during regular season

• FGM: Field Goals Made

• FGA: Field Goal Attempts

• Points3: 3-Point Field Goals

• Points3_atts: 3-Point Field Goal Attempts

• Points2: 2-Point Field Goals

• Points2_atts: 2-Point Field Goal Attempts

• FTM: Free Throws Made

• FTA: Free Throw Attempts

• OREB: Offensive Rebounds

• DREB: Defensive Rebounds

• AST: Assists

• STL: Steals

• BLK: Blocks

• TO: Turnovers

• GP: Games Played

**Calculated column names and variables added to the data frame imported from nba2017-player-statistics.csv:**

• EFF: Efficiency statistic calculated through: (PTS + REB + AST + STL + BLK - Missed FG - Missed FT - TO) / GP

• Missed FG: missed field goals, calculated through FGA - FGM

• Missed FT: missed free throws, calculated through FTA - FTM

• PTS: total points, calculated through a weighted point total (x2 for 2-pointers, x3 for 3-pointers, x1 for free throws)

• REB: total rebounds: offensive and defensive. Calculated through OREB + DREB

• MPG: Average minutes per game. Calculated through MIN / GP

**Data structures imported and created:**

• dataset1: a data frame imported from the data source using "read.csv()"

• dataset2: a data frame imported from the data source using "read_csv()"; also the data frame used for all calculations in the homework.

• topten_eff: a data frame created from selecting columns and filtering rows from dataset2 to obtain the top 10 EFF values, and then sorted in descending order.

• neg_eff: a data frame created from selecting columns and filtering rows from dataset2 to obtain all players with EFF < 0.

• corr_coeff: a vector containing the correlation coefficients between EFF and PTS, REB, STL, AST, BLK, Missed_FT, Missed_FG, and TO.

• sorted_eff: corr_coeff sorted in descending order.
