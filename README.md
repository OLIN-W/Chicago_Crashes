# Chicago_Crashes

# Chicago Crashes: Phase 3 Project

## Overview

This project analyzes vehicle crash data from Chicago to identify and rank the key environmental, temporal, and behavioral factors that contribute most to crash severity. The goal is to inform the City of Chicago Department of Transportation (CDOT) on effective policy and road safety strategies by predicting crash severity categories using machine learning.

## Stakeholder

- **City of Chicago Department of Transportation (CDOT)**

## Business Problem

Identify and rank the most influential factors (environmental, temporal, behavioral) that contribute to the severity of vehicle crashes, enabling data-driven interventions to reduce severe outcomes.

## Data Sources

- `Traffic_Crashes_-_Crashes_20250605.csv`
- `Traffic_Crashes_-_People_20250606.csv`

## Target Variable

- `MOST_SEVERE_INJURY` (severity of crash outcome)

## Approach

1. **Data Preparation**
   - Merged crash and people datasets on `CRASH_RECORD_ID`
   - Selected relevant features and handled missing values
   - Encoded categorical variables and target labels

2. **Exploratory Data Analysis**
   - Visualized severity distributions and key factor relationships
   - Identified patterns in weather, lighting, roadway conditions, and time of day

3. **Modeling**
   - Baseline: Dummy Classifier
   - Logistic Regression (with scaling and hyperparameter tuning)
   - Decision Tree (with hyperparameter tuning)
   - Random Forest (with class balancing and hyperparameter tuning)
   - Evaluated models using accuracy, precision, recall, F1-score, and confusion matrices

4. **Feature Importance**
   - Identified top predictors for severe crashes using Random Forest feature importances

## Key Insights

- Most crashes occur in clear weather and daylight, but severe injuries are more likely in rain, fog, and low-light conditions.
- Dry roads have the most crashes, but wet, icy, or snowy roads increase severity risk.
- Human factors (e.g., distracted or impaired driving) are significant contributors to severe outcomes.
- Fatal and incapacitating injuries are rare but can be predicted with reasonable accuracy.

## Recommendations for CDOT

1. **Target High-Risk Conditions**
   - Improve signage, lighting, and signals during adverse weather and nighttime.
   - Implement temporal interventions (e.g., speed reductions, increased patrols).

2. **Behavioral Campaigns**
   - Educate the public on distracted/impaired driving dangers.
   - Promote safe driving even in seemingly safe conditions.

3. **Model-Driven Planning**
   - Integrate predictive models into real-time systems to flag high-risk situations.
   - Dynamically allocate resources (EMS, road maintenance) based on model outputs.

## How to Run

1. Install required Python libraries (see notebook for details).
2. Place the datasets in the project directory.
3. Open and run the Jupyter notebook `Chicago_crash.ipynb` step by step.




