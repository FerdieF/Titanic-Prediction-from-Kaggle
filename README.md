# Titanic-Prediction-from-Kaggle

## 📊 Exploratory Data Analysis (EDA) — Narrative

During the exploration of the Titanic dataset, several patterns emerged that strongly influenced passenger survival outcomes.

1. Gender Plays the Most Significant Role

One of the clearest insights is the survival gap between male and female passengers.
From the barplot, female passengers had a dramatically higher survival rate compared to males. This aligns with the historical evacuation principle “women and children first”, which strongly favored female passengers during lifeboat boarding.

2. Passenger Class Strongly Affects Survival

Passenger class (Pclass) also shows a distinct impact.
First–class passengers had the highest likelihood of survival, followed by second class, while third–class passengers had the lowest. This reflects socioeconomic disparities in cabin location, accessibility to lifeboats, and priority during evacuation.

3. Combined Effect: Gender × Pclass

When examining gender and class together, the inequality becomes even more pronounced:

Female passengers in 1st and 2nd class had the highest survival rates, often nearing 100%.

Male passengers in 3rd class had the lowest survival probability of all groups.

This combination highlights how social and economic factors together shaped evacuation outcomes.

4. Correlation Heatmap Confirms Key Relationships

The heatmap indicates:

A strong negative correlation between Sex_Encoded and survival — reinforcing that females were much more likely to survive.

## 🔧 Data Preprocessing — Narrative

Before building the prediction model, several preprocessing steps were performed to ensure the dataset was clean, consistent, and ready for machine learning.

1. Handling Missing Data

The dataset contained missing values in several columns, most notably in:

Age (≈20% missing)

Fare (missing in test set)

Cabin (≈77% missing)

To handle this:

Age was imputed using the median, as it’s more robust to outliers than the mean.

Fare in the test set was also filled using the median.

Cabin was dropped entirely due to its extremely high missing percentage and low predictive power.

This preprocessing ensures the machine learning model receives complete numerical features without NaN values.

2. Encoding Categorical Variables

Machine learning models require numerical input, so categorical features were converted:

Sex → Sex_Encoded

male = 1

female = 0

Embarked → One-hot encoding

Embarked_Q

Embarked_S
(Embarked_C digunakan sebagai baseline)

This encoding allows the model to interpret these values correctly.

3. Standardized Feature Selection

After cleaning and encoding, a consistent set of features was used for training:

Pclass

Sex_Encoded

Age_final

SibSp

Parch

Fare

Embarked_Q

Embarked_S

These variables were chosen due to both their interpretability and predictive potential, according to the EDA results.
A moderate negative correlation between Pclass and survival — showing that lower-class passengers faced greater risk.

Other variables show only weak or negligible correlation with survival.

These findings help identify the most influential features when building a predictive model.

## 🤖 Modeling & Evaluation — Narrative

A baseline machine learning model was developed to predict whether a passenger survived the Titanic disaster.

1. Model Used

The project uses Logistic Regression, a simple yet effective algorithm for binary classification. It is:

Interpretable

Fast to train

Works well with linearly separable features

This makes it a good baseline before trying more complex models.

2. Training Setup

The dataset was split into:

80% training data

20% validation data

This ensures that the model can be evaluated on unseen data and prevents overfitting.

3. Model Performance

The model’s performance was measured using:

Accuracy

Precision

Recall

F1-score

A confusion matrix was also analyzed to understand misclassification patterns, especially between survivors and non-survivors.

While logistic regression provides a solid starting point, it also reveals areas where more advanced models or additional feature engineering may boost performance.

4. Generating Predictions

After training and validating the model, predictions were generated for test.csv, producing a file:

submission_logreg.csv


This file follows Kaggle’s required format and can be submitted directly to the Titanic competition.

## 📝 Project Summary — Narrative

This project demonstrates the full workflow of a classic machine learning classification problem:

Cleaning and preparing real-world data

Exploring patterns and relationships

Encoding and selecting features

Training and evaluating a baseline model

Producing reproducible predictions

The Titanic dataset remains a popular benchmark for introducing data science concepts, and this project provides a clean, structured, and beginner-friendly approach.
