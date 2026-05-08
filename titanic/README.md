# 🚢 Titanic — Survival Prediction

> Kaggle competition: [Titanic - Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic/overview)

## Overview

On April 15, 1912, the RMS Titanic sank after colliding with an iceberg, killing 1,502 of 2,224 passengers and crew. While survival involved some luck, certain groups had notably higher chances.

**Goal:** build a model to predict which passengers survived, using features like age, sex, and passenger class.

## Dataset Description

### Overview

The dataset is divided into two groups:

- `train.csv` — training dataset
- `test.csv` — testing dataset

The training set is used to build machine learning models.  
For this dataset, the target variable (`Survived`) is provided for each passenger.

The model uses passenger features such as:
- gender,
- ticket class,
- age,
- fare,
- among others.

Feature engineering techniques can also be applied to create additional predictive variables.

The test set is used to evaluate the model on unseen data.  
In this dataset, the target variable is not provided, and the objective is to predict passenger survival.

Additionally, the competition provides:

- `gender_submission.csv`

This file contains an example submission where all female passengers survive and all male passengers do not.

---

## Data Dictionary

| Variable | Definition | Key |
|---|---|---|
| `Survived` | Survival | 0 = No, 1 = Yes |
| `Pclass` | Ticket class | 1 = 1st, 2 = 2nd, 3 = 3rd |
| `Sex` | Passenger sex | — |
| `Age` | Age in years | — |
| `SibSp` | Number of siblings/spouses aboard | — |
| `Parch` | Number of parents/children aboard | — |
| `Ticket` | Ticket number | — |
| `Fare` | Passenger fare | — |
| `Cabin` | Cabin number | — |
| `Embarked` | Port of Embarkation | C = Cherbourg, Q = Queenstown, S = Southampton |

---

## Variable Notes

### `Pclass`

`Pclass` represents a proxy for socio-economic status (SES):

- 1st class → Upper class
- 2nd class → Middle class
- 3rd class → Lower class

---

### `Age`

- Age values may be fractional for infants.
- Estimated ages are represented as values ending in `.5`.

---

### `SibSp`

Defines family relationships aboard the Titanic:

- Sibling → brother, sister, stepbrother, stepsister
- Spouse → husband, wife

Fiancés and mistresses were not included.

---

### `Parch`

Defines parent/child relationships aboard the Titanic:

- Parent → mother, father
- Child → daughter, son, stepdaughter, stepson

Some children traveled only with a nanny, therefore having `Parch = 0`.

## Workflow

1. Exploratory Data Analysis
2. Feature Engineering
3. Preprocessing Pipeline
4. Model Training & Tuning
5. Results & Submission

## Conclusion 

This project demonstrated the complete workflow of a machine learning problem:

- data exploration;
- preprocessing;
- feature engineering;
- pipeline construction;
- hyperparameter optimization.

The final Random Forest model achieved competitive Kaggle performance (0.7808 score) while maintaining a clean and reproducible workflow.