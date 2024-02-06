# Data
-   **[Dataset]**: The 2021–2022 English Premier League (EPL) season's match-day statistics are contained in this dataset, which is sourced from Evan Gower's work on Kaggle. It is taken from the official Premier League website and has been carefully cleaned. It includes 380 matches, which represents the whole season. Every entry contains an abundance of information, such as the teams involved, the date of the match, the referee, and a variety of in-game statistics for both the home and away sides, including goals, shots, fouls, and cards. It also provides full-time results and halftime analytics, providing a detailed analysis of each match's dynamics. This dataset offers a basis for more in-depth research into the variables impacting team performance and match results in addition to providing a numerical narrative of the season.

# Codebook for [chosen] Dataset
```{r}
# Get the Data

# Read in with tidytuesdayR package 
# Install from CRAN via: install.packages("tidytuesdayR")
# This loads the readme and all the datasets for the week of interest

# Either ISO-8601 date or year/week works!

tuesdata <- tidytuesdayR::tt_load('2023-04-04')
tuesdata <- tidytuesdayR::tt_load(2023, week = 14)

soccer <- tuesdata$soccer

# Or read in the data manually

soccer <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-04-04/soccer21-22.csv')
```

## Variable Names, Data type and Descriptions:

|variable |class     |description |
|:--------|:---------|:-----------|
|Date     |character |The date when the match was played  |
|HomeTeam |character |The home team    |
|AwayTeam |character |The away team    |
|FTHG     |double    |Full time home goals        |
|FTAG     |double    |Full time away goals        |
|FTR      |character |Full time result         |
|HTHG     |double    |Halftime home goals        |
|HTAG     |double    |Halftime away goals        |
|HTR      |character |Halftime results         |
|Referee  |character |Referee of the match    |
|HS       |double    |Number of shots taken by the home team          |
|AS       |double    |Number of shots taken by the away team          |
|HST      |double    |Number of shots on target by the home team   |
|AST      |double    |Number of shots on target by the away team   |
|HF       |double    |Number of fouls by the home team   |
|AF       |double    |Number of fouls by the away team    |
|HC       |double    |Number of corners taken by the home team |
|AC       |double    |Number of corners taken by the away team |
|HY       |double    |Number of yellow cards received by the home team |
|AY       |double    |Number of yellow cards received by the away team  |
|HR       |double    |Number of red cards received by the home team  |
|AR       |double    |Number of red cards received by the away team  |




