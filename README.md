# IPL Score Prediction Using Linear Regression

A Machine Learning project that predicts the final score of an IPL innings using historical match data and live match conditions.

## Table of Contents
- Overview
- Problem Statement
- Dataset
- Features
- Models Used
- Model Performance
- Project Workflow
- Sample Prediction
- Requirements
- How to Run
- Results
- Future Scope
- References

## Overview
Cricket, especially the Indian Premier League (IPL), is a fast-paced and unpredictable game. This project uses machine learning to predict the total score of an innings based on match conditions such as runs, wickets, overs, and recent performance.

The project compares four regression models:
- Linear Regression
- Support Vector Regression
- K-Nearest Neighbors Regressor
- Decision Tree Regressor

## Problem Statement
The goal of this project is to predict the final score of an IPL innings using match data.  
The model helps estimate the score at a given stage of the innings and can be useful for cricket analysts, fans, and broadcasters.

## Dataset
The dataset contains ball-by-ball IPL data with 76,014 rows and 15 columns.

### Important Columns
- `bat_team`
- `bowl_team`
- `runs`
- `wickets`
- `overs`
- `runs_last_5`
- `wickets_last_5`
- `total`

### Removed Irrelevant Columns
- `mid`
- `date`
- `venue`
- `batsman`
- `bowler`
- `striker`
- `non-striker`

### Preprocessing Steps
- Removed first 5 overs of every match.
- Applied label encoding to team names.
- Prepared the data for regression modeling.

## Features
- Predict IPL innings score
- Compare multiple regression models
- Use historical match data
- Predict score from live match inputs
- Display model evaluation metrics

## Models Used

### 1. Linear Regression
A basic and interpretable regression model that finds a linear relationship between the input features and the target score.

### 2. Support Vector Regression
A regression version of SVM that can handle complex relationships in the data.

### 3. K-Nearest Neighbors Regressor
Predicts the score based on the nearest similar match situations.

### 4. Decision Tree Regressor
Splits the data into branches based on conditions and gives interpretable predictions.

## Model Performance

| Model | Train Score | Test Score | MAE | RMSE |
|------|-------------|-----------|-----|------|
| Decision Tree Regressor | 99.98% | 85.64% | 3.92 | 11.29 |
| Linear Regression | 65.97% | 65.64% | 13.13 | 17.46 |
| Support Vector Regression | 57.44% | 57.51% | 14.65 | 19.42 |
| K-Nearest Neighbors Regressor | 86.56% | 78.52% | 9.66 | 13.81 |

## Project Workflow
1. Import the dataset.
2. Perform exploratory data analysis.
3. Remove irrelevant columns.
4. Remove the first 5 overs from each match.
5. Encode categorical variables.
6. Split the data into training and testing sets.
7. Train regression models.
8. Evaluate model performance.
9. Predict final scores using live match inputs.

## Sample Prediction

### Input
- Batting Team: Mumbai Indians
- Bowling Team: Kings XI Punjab
- Overs: 12.3
- Runs: 113
- Wickets: 2
- Runs in last 5 overs: 55
- Wickets in last 5 overs: 0

### Output
- Predicted Score: 184
- Actual Score: 176

## Requirements
Install the following Python libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## How to Run
1. Clone the repository.
2. Install the required libraries.
3. Open the notebook or Python file.
4. Run the preprocessing and model training cells.
5. Enter match details to get the predicted score.

## Results
The Decision Tree Regressor performed the best among the tested models with the highest test score and lowest error values. Linear Regression was used as a baseline model. SVR and KNN also provided useful comparisons for performance analysis.

## Future Scope
- Use deep learning models such as LSTM and RNN.
- Add real-time match data integration.
- Improve accuracy with more feature engineering.
- Build a web app for live score prediction.

## References
- [IPLScorePredictor GitHub Repository](https://github.com/zep-analytics/IPLScorePredictor.git)
- [IJFMR Paper](https://www.ijfmr.com/papers/2023/6/8241.pdf)
- [Kaggle Notebook](https://www.kaggle.com/code/nitinkumarsingh123/ipl-scoreprediction)
