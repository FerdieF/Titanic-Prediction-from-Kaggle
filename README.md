# Titanic-Prediction-from-Kaggle

📊 Exploratory Data Analysis (EDA) — Narrative

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

A moderate negative correlation between Pclass and survival — showing that lower-class passengers faced greater risk.

Other variables show only weak or negligible correlation with survival.

These findings help identify the most influential features when building a predictive model.
