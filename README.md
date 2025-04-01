# Fantasy Premier League (FPL) Team Optimization

This project aims to build a predictive model for Fantasy Premier League (FPL) player selection based on historical performance data. The goal is to use machine learning to predict players' total points and then optimize team selection under various constraints (such as budget, positions, and team selection rules).

## Project Overview

This repository includes:
- Data fetching from the FPL API
- Data processing and feature engineering
- Predicting FPL player points using a **Random Forest Regressor**
- Optimizing team selection using **Linear Programming (PuLP)**

## Features

1. **Data Fetching:**  
   The project uses the [FPL API](https://fantasy.premierleague.com/api/bootstrap-static/) to get player data such as goals, assists, transfers, and more.

2. **Machine Learning Model:**  
   A **Random Forest Regressor** is trained on player features (e.g., goals, assists, cost, transfers) to predict the total points for each player.

3. **Team Optimization:**  
   The **PuLP** library is used to solve the optimization problem where the objective is to maximize predicted points while adhering to:
   - **Budget Constraints**
   - **Position Constraints (e.g., number of forwards, defenders)**
   - **Team Constraints (maximum number of players per team)**
   - **Total Players Constraint**  

4. **Visualization:**  
   The project includes visualizations for:
   - Distribution of total points of players
   - Feature importance of various player attributes for prediction
   - Position distribution of the selected team
   - Predicted points for the players in the selected team

## Requirements

- Python 3.x
- Libraries:
  - `requests`
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`
  - `pulp`

You can install the necessary libraries using `pip`:

```bash
pip install requests pandas numpy matplotlib seaborn scikit-learn pulp
