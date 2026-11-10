# Predicting NCAA Women's Basketball Tournament Outcomes

**Data Science · Machine Learning · R · Multiclass Classification**

## Overview

Can a team's regular-season performance help predict how far it will advance in the NCAA Division I Women's Basketball Tournament?

This individual data science project investigates whether **regional win percentage** and **conference win percentage** can be used to predict a team's **tournament finish**. I explored historical tournament data, prepared a classification-ready dataset, trained a K-Nearest Neighbours (KNN) model, and evaluated its performance across multiple tournament outcomes.

The project illustrates an end-to-end introductory machine learning workflow—from exploratory data analysis to model selection and critical evaluation—while highlighting the limitations of predicting rare sporting outcomes from a small set of features.

## Research Question

> Can regional win percentage and conference win percentage predict a team's NCAA Women's Basketball Tournament finish?

## Data

The analysis uses an adapted historical NCAA Division I Women's Basketball Tournament dataset spanning **1982–2018**, with **2,092 records** before preprocessing.

- **Features:** Regional win percentage and conference win percentage
- **Target:** Tournament finish, represented by eight categories from opening-round loss through champion
- **Source:** [Women's March Madness dataset — Diverse Data Hub](https://github.com/diverse-data-hub/diversedata/blob/main/data-clean/womensmarchmadness.csv)

## Approach

1. **Data preparation:** Selected relevant variables, examined missing values, and prepared the tournament-finish categories.
2. **Exploratory analysis:** Investigated win-percentage distributions, class frequencies, and relationships between performance and tournament outcomes.
3. **Model development:** Built a multiclass KNN classifier using standardized numerical predictors.
4. **Model selection:** Used a stratified **75/25 train–test split** and **5-fold cross-validation** on the training set to tune the number of neighbours.
5. **Evaluation:** Assessed held-out predictions using accuracy, macro precision, macro recall, and a confusion matrix.

## Results

| Evaluation metric | Test-set result |
| --- | ---: |
| Accuracy | **48.13%** |
| Macro precision | 33.54% |
| Macro recall | 18.87% |
| Selected KNN neighbours | **77** |

**Key finding:** The model identifies some broad patterns in more common tournament outcomes but struggles to distinguish less frequent, deep-tournament finishes. Class imbalance and the limited predictive information contained in just two win-percentage features restrict its reliability.

These findings are an analysis of model limitations—not a claim that the model can reliably forecast tournament results.

## Tools & Skills

**R · Jupyter Notebook · tidyverse · tidymodels · ggplot2 · kknn · yardstick**

Skills demonstrated include data cleaning, exploratory data analysis, data visualization, feature scaling, train–test splitting, cross-validation, hyperparameter tuning, multiclass classification, and model evaluation.

## Lessons Learned

A single performance metric does not tell the whole story. Although the model achieved approximately 48% accuracy, the confusion matrix and class-level evaluation revealed a tendency to predict common outcomes rather than rare tournament finishes.

A useful next step would be to explore additional features—such as tournament seed and other team-performance indicators—and compare KNN against alternative classification approaches.

## Project Access

The original notebook and implementation are maintained in a **private repository** because this project was completed as academic coursework. This public README is a portfolio overview rather than a distribution of the assignment or its source code.

For questions about the methodology or a private review of the work, please contact the repository owner.
