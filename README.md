🍷 Wine Quality Prediction – Machine Learning Project

This project is about predicting whether a wine is good or bad based on its chemical properties.
I used the given winequality.csv dataset and applied the full ML workflow from start to end.

The main idea of the project is to understand how real ML projects are done, not just run a model.

📌 Project Overview

The dataset contains different chemical measurements of wine (like acidity, sugar, pH etc.) and a quality score.
Since predicting the exact score is difficult and not very useful, I converted it into a binary classification:

Quality ≥ 7 → Good wine

Quality < 7 → Bad wine

Then I trained multiple ML models and compared their performance.

📂 Dataset

File: winequality.csv

Each row = one wine sample

All columns (except quality) = numerical chemical values

Quality column = score given by tasters

📝 Steps I Performed
1. Loading the Dataset

Imported pandas, numpy, seaborn, matplotlib, scikit-learn

Loaded the CSV and checked first/last/random rows

This helped me understand what type of data I was dealing with

2. Data Inspection

Checked column names, shape, and data types

Used describe() to see summary stats

Inspection helped me confirm the dataset is clean and numerical

3. Missing Values Check

Used isnull().sum()

No major missing values were found

If missing values existed, I would've filled them or removed rows

4. EDA (Exploratory Data Analysis)

Checked how many samples belong to each quality score

Plotted count graph for the quality column

Observation:
Most wines fall in the middle quality range → dataset is slightly imbalanced.

5. Converting to Binary Classification

Created a new column called quality_label.

1 → Good

0 → Bad

This made the problem simpler and more practical.

6. Separating Features and Target

X = all chemical features

y = the new quality_label column

I did not use the original quality column to avoid leaking answers

7. Train/Test Split

80% training

20% testing

random_state = 42 for consistent results

Splitting data helps check how the model performs on unseen data.

8. Feature Scaling

Used StandardScaler

Fit only on training data, then transformed both sets

Scaling is important especially for KNN, SVM, and Logistic Regression.

9. Model Training

Trained 5 models:

Logistic Regression

KNN

Decision Tree

Random Forest

SVM

Each model works differently and learns patterns in its own way.

10. Model Comparison

Calculated accuracy for all models and compared them.

Best models:

Random Forest

SVM

They handled the data better and gave higher accuracy.

11. Pipeline + Hyperparameter Tuning

Created a pipeline (scaling + model) and tuned SVM using GridSearchCV.
This helped find the best settings automatically.

✔ Final Conclusion

The dataset contains chemical details of wine samples

EDA showed the classes are imbalanced

Binary classification made the task more meaningful

Random Forest and SVM gave the best performance

I learned how scaling, model selection, and tuning affect accuracy

The whole process is similar to how ML projects are done in real companies

🔧 Tools & Libraries

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-Learn
