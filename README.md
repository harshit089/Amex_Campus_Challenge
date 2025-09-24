# American Express Campus Challenge 2024 - T20 Cricket Match Prediction

This repository contains the code and documentation for the **American Express Campus Challenge 2024**, focusing on predicting the winning team in T20 cricket matches using machine learning models.

## Objective

The goal of this challenge is to build the best machine learning model that accurately predicts the winning team for T20 cricket matches based on historical match data, including detailed batsman and bowler statistics.

## Project Overview

- **Dataset**: Historical T20 match data (domestic and international) from 2021 to 2023, including detailed scorecards for batsmen and bowlers.
- **Task**: Use boosting algorithms (e.g., XGBoost, LightGBM) to develop a model that predicts the winning team based on various game-level and player-level features.
- **Evaluation**: Models are evaluated based on accuracy, with predictions being compared to the actual outcomes of matches in the test set.

## Data Breakdown

- **Training Data**: Contains match-level information (948 rows, 23 columns).
- **Additional Data**:
  - **Match-level**: 1689 rows, 30 columns (2021-2023).
  - **Batsman-level**: 24,483 rows, 21 columns.
  - **Bowler-level**: 18,539 rows, 18 columns.

## Key Features

- **Match-level features**: `match_id`, `team1_id`, `team2_id`, `winner_id`, `toss_winner`, `toss_decision`, `venue`, `city`, `match_dt`, along with ratios and win percentages like `team_count_50runs_last15`, `team_winp_last5`, and `ground_avg_runs_last15`.
- **Batsman-level features**: `match_id`, `batsman_id`, `inning`, `runs`, `balls_faced`, `strike_rate`, etc.
- **Bowler-level features**: `match_id`, `bowler_id`, `inning`, `runs_conceded`, `wicket_count`, `economy`, etc.

## Approach

- **Boosting Algorithms**: Focus on XGBoost, LightGBM, and ensemble models.
- **Feature Engineering**: Use the detailed player-level data (batsman and bowler statistics) to engineer meaningful features that improve model performance.
- **Validation**: Employ cross-validation and holdout validation techniques to ensure the model generalizes well and avoids overfitting.

## Submission Format

1. **File 1**: Contains predictions for the evaluation dataset.
2. **File 2**: Contains predictions for the training data and details of the models used, including the top 10 features.

## Repository Contents

- **Data Preprocessing**: Scripts for cleaning and preparing the data.
- **Feature Engineering**: Scripts for generating custom features from batsman and bowler data.
- **Model Training**: Code for training boosting models and tuning hyperparameters.
- **Evaluation**: Scripts for validating model performance and generating submission files.

## Competition Structure

- **Round 1**: Model training on provided labeled data, followed by evaluation on unseen test data.
- **Round 2**: Similar to Round 1 with a different dataset.
- **Final Round**: Participants submit a deck presentation outlining their approach.

## How to Run

1. Clone this repository.
   ```bash
   git clone https://github.com/Rishii-jain/amex-campus-challenge-2024.git
   cd amex-campus-challenge-2024
