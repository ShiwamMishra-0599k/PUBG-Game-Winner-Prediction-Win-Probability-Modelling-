# PUBG Game Winner Prediction — Win Probability Modelling

This project aims to predict the win percentage of PUBG players based on their in-game performance statistics.
Using machine learning, the project identifies the most important variables influencing win probability and evaluates multiple models to determine the best one for real-world deployment.

# Tech Stack
## Programming
- Python (Pandas, NumPy, Scikit-learn)
- Jupyter Notebook
- Machine Learning
- Linear Regression
- Random Forest Regressor
- XGBoost
- Decision Tree
- Ensemble Techniques

#Data Source

Dataset Link (Provided by Rubixe):
https://d3ilbtxij3aepc.cloudfront.net/projects/CDS-Capstone-Projects/PRCP-1012-GameWinnerPred.zip

## Dataset Includes
29 attributes such as:
1.	Id
2.	groupId
3.	matchId
4.	assists
5.	boosts
6.	damageDealt
7.	DBNOs
8.	headshotKills
9.	heals
10.	killPlace
11.	killPoints
12.	kills
13.	killStreaks
14.	longestKill
15.	matchDuration
16.	matchType
17.	maxPlace
18.	maxPlace
19.	rankPoints
20.	revives
21.	rideDistance
22.	roadKills
23.	swimDistance
24.	teamKills
25.	vehicleDestroys
26.	walkDistance
27.	weaponsAcquired
28.	winPoints
29.	winPlacePerc


# Problem Statement
## Objective - To predict the win probability (winPlacePerc) of a PUBG player using match statistics and behavioral patterns.

# Task Breakdown
- Task 1: Complete EDA report
- Task 2: Build ML models to predict winPlacePerc
- Task 3: Compare model performance & identify best model
- Task 4: Document challenges and mitigation techniques

# Goal of the Project
- Understand PUBG player performance metrics
- Identify what makes players win
- Build a predictive model to estimate win probability
- Evaluate performance of different ML algorithms
- Provide insights for game strategy optimization

# Solution Approach
## ✔ Step 1: Data Cleaning
- Removed duplicates
- andled missing values (mean/median imputation)
- Eliminated impossible values (e.g., negative damage, extreme outliers)
- Managed skewed numeric data using transformations

## ✔ Step 2: EDA & KPI Analysis
- Kill distribution analysis
- Movement metrics (walk/ride/swim distance)
- Correlation matrix
- Match type performance
- Ranking behavior

## ✔ Step 3: Feature Engineering
Created new features:
- CombatScore (kills + damageDealt)
- MobilityScore (walkDistance + rideDistance)
- SupportScore (heals + boosts)
- SurvivalTime metrics

## ✔ Step 4: Model Development
Tested algorithms:
- Linear Regression
- Random Forest
- XGBoost
- Decision Tree
- Ensemble Models

## ✔ Step 5: Evaluation
Evaluated with:
- R2 Score
- Mean_Squared_Error
- Mean_Absolute_Error
- Cross-validation performance

# Key Insights & Findings
- walkDistance is the strongest predictor of win probability.
- Aggressive players (high damage & kills) tend to rank higher.
- Mobility significantly impacts survival.
- Random Forest & XGBoost delivered the best accuracy and most stable performance.

# Challenges & Solutions

| Challenge                            | Solution                                  |
| ------------------------------------ | ----------------------------------------- |
| Heavy outliers (extreme match stats) | Applied winsorization & robust scaling    |
| Missing winPlacePerc values          | Imputed using median grouped by matchType |
| High dimensionality                  | Feature selection & VIF analysis          |
| Skewed numeric distribution          | Log transformation & normalization        |
| Model overfitting                    | Cross-validation + regularization         |


# Impact & Applications
- Real-time win probability estimation
- Player performance evaluation
- Esports analytics & strategy optimization
- AI-powered gaming insights
- Player matchmaking improvement
