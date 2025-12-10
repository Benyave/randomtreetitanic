
# 🚢 Titanic - Machine Learning from Disaster

This repository contains a beginner-friendly solution for the famous Kaggle competition: **Titanic - Machine Learning from Disaster**. The script analyzes passenger data to predict who survived the shipwreck using a **Random Forest Classifier**.

## 📋 Project Overview

The goal of this project is to build a predictive model that answers the question: "what sorts of people were more likely to survive?" using passenger data (ie name, age, gender, socio-economic class, etc).

### Key Features
* **Data Handling:** Uses `Pandas` and `NumPy` for data manipulation.
* **Exploratory Data Analysis (EDA):** Calculates and prints survival rates based on gender.
* **Feature Engineering:** Uses One-Hot Encoding (`pd.get_dummies`) to convert categorical variables into a numeric format.
* **Modeling:** Implements a `RandomForestClassifier` from Scikit-Learn.

## 🛠️ Technologies Used

* Python 3.x
* [Pandas](https://pandas.pydata.org/) (Data manipulation)
* [NumPy](https://numpy.org/) (Linear Algebra)
* [Scikit-Learn](https://scikit-learn.org/) (Machine Learning)

## 📂 Dataset

The model uses the standard Kaggle dataset:
* `train.csv`: Used to train the model.
* `test.csv`: Used to generate predictions.

*Note: The script assumes the input files are located in `/kaggle/input/titanic/`. If you are running this locally, you may need to adjust the file paths in `pd.read_csv`.*

## ⚙️ How It Works

1.  **Data Loading:** Reads the training and testing datasets.
2.  **Basic Analysis:** Calculates the survival rate for men vs. women to establish a baseline understanding (Women had a ~74% survival rate vs. ~18% for Men).
3.  **Preprocessing:**
    * Selects specific features: `["Pclass", "Sex", "SibSp", "Parch"]`.
    * Converts the `Sex` column into dummy variables (0/1) for the model.
4.  **Model Training:**
    * Algorithm: **Random Forest Classifier**
    * Estimators (Trees): 100
    * Max Depth: 5
5.  **Prediction:** Generates predictions for the test set and saves the results to `submission.csv`.

## 🚀 Getting Started

### Prerequisites

Make sure you have Python installed. You can install the required libraries using pip:

```bash
pip install pandas numpy scikit-learn
