# Crocodilian Species Prediction


## Overview
This project builds a machine learning pipeline to predict the species of crocodilians based on ecological and biological observations. Using decision trees, random forests, and gradient boosting classifiers, the project explores feature engineering, model evaluation, and hyperparameter tuning. The dataset used contains labeled crocodilian observations.

## Dataset
The dataset used is `crocodile_dataset.csv`, containing information on observed crocodilians. Columns such as `Observation ID`, `Scientific Name`, and observer metadata were dropped to focus on features available during immediate inspection. Categorical variables were one-hot encoded for model training.

## Features and Labels
- **Features (X):** Length, Weight, Habitat type, region, sex, and age class after one-hot encoding.  
- **Labels (Y):** The `Common Name` of the crocodilian species.

## Methodology
1. Data preprocessing (dropping irrelevant columns, encoding categorical variables).  
2. Train/test split using an 80/20 ratio.  
3. Model selection and evaluation using cross-validation for:
   - Decision Tree Classifier  
   - Random Forest Classifier  
   - Gradient Boosting Classifier  
4. Gradient Boosting was identified as the best-performing model.  
5. Hyperparameter tuning was performed on:
   - Number of estimators  
   - Maximum tree depth  
   - Learning rate  
6. Final evaluation included training time comparison and confusion matrix visualization.

## Results
Gradient Boosting Classifier achieved the best accuracy compared to Decision Tree and Random Forest classifiers. Hyperparameter tuning revealed optimal values of:

- `n_estimators = 50`  
- `max_depth = 3`  
- `learning_rate = 0.1`  

The final model demonstrated near-perfect classification performance, with the main misclassification occurring between the **New-Guinea Crocodile** and **Hall’s New-Guinea Crocodile**.

## Visualizations
The project includes visualizations for:
- Accuracy vs Number of Estimators  
- Accuracy vs Max Depth  
- Accuracy vs Learning Rate  
- Confusion Matrix of final model predictions  

## Dependencies
- Python 3.x  
- pandas  
- numpy  
- scikit-learn  
- matplotlib  

## Usage
1. Ensure `crocodile_dataset.csv` is placed in the working directory.  
2. Install required dependencies using:  
   ```bash
   pip install pandas numpy scikit-learn matplotlib
   ```  
3. Run the notebook or script to execute preprocessing, training, evaluation, and visualization.
