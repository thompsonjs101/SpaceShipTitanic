# 🛸 Spaceship Titanic - Passenger Transport Prediction

This project analyzes and models passenger data from a fictional interstellar transport vessel, **Spaceship Titanic**, to predict whether passengers were **transported** to another dimension during the voyage.

## 📁 Files

- `main.py` or `main.ipynb`: Core script that handles preprocessing, feature engineering, model training, and prediction.
- `train.csv`: Training dataset with known outcomes.
- `test.csv`: Test dataset without known outcomes (for final submission).
- `submission.csv`: Output file containing Passenger IDs and predicted transport outcomes.

## 🧠 Project Overview

### Goal

Predict the `Transported` status (True/False) of passengers based on provided attributes such as spending habits, cabin location, and demographics.

## 🛠️ Key Steps

### 1. **Data Loading & Cleaning**
- Merged `train.csv` and `test.csv` for unified preprocessing.
- Removed non-predictive columns (`Name`, `PassengerId`).

### 2. **Feature Engineering**
- Split `Cabin` into `Deck`, `Num`, and `Side`.
- Encoded categorical variables (`Deck`, `Side`, `HomePlanet`, `Destination`).
- Created new features from spending columns (`AmtSpent`, `StdAmtSpent`, `MeanAmtSpent`).
- Combined relevant features to form `3_high_cols` and `3_low_cols`.

### 3. **Imputation**
- Handled missing values using KNN imputation for numerical features and placeholders for categorical ones.

### 4. **Model Training**
Trained and compared the following models:
- XGBoost
- Decision Tree
- Random Forest
- Logistic Regression
- LightGBM

Performance was evaluated using **accuracy score** on a validation split.

### 5. **Prediction & Submission**
- Generated predictions on the test set using the best-performing model.
- Created `submission.csv` for upload to the competition platform.

## 📊 Requirements

Install dependencies via `pip`:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm
```

## 🚀 How to Run

1. Place `train.csv` and `test.csv` in the working directory.
2. Run `main.py` or the notebook.
3. `submission.csv` will be generated with predictions.

## 📌 Notes

- Placeholder values like `'U'` and `-1` are used to represent unknown categories during encoding.
- Model comparison is printed directly after training.
- One-hot encoding is applied after imputation and categorical filling.

## 🧾 License

This project is released under the MIT License.
