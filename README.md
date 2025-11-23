# Elevatelabs-task6
📘 README – Diabetes Dataset KNN Classification with Preprocessing, EDA & PCA Visualization
📌 Project Overview

This project applies K-Nearest Neighbors (KNN) classification on the Diabetes dataset from Plotly.
The workflow demonstrates:

Data loading from a valid URL

Handling missing values

Replacing zero values with NaN (common in medical datasets)

Imputing missing data using Mean, Median, and Mode

Exploratory Data Analysis (EDA)

Scaling features using StandardScaler

Tuning K (1 to 15) to find the best accuracy

Training the KNN classifier for all 3 imputation strategies

Plotting accuracy vs K

Visualizing decision boundaries using PCA (2 Components)

This gives a complete end-to-end ML pipeline for classification tasks.

📂 Dataset Information

The dataset used is the Diabetes Dataset from Plotly.

📌 Valid Dataset URL:

https://raw.githubusercontent.com/plotly/datasets/master/diabetes.csv

Features

The dataset contains 8 numerical medical attributes:

Pregnancies

Glucose

BloodPressure

SkinThickness

Insulin

BMI

DiabetesPedigreeFunction

Age

Target

Outcome = 0 → No Diabetes

Outcome = 1 → Diabetes Present

🧹 Data Preprocessing Steps
✔ Step 1: Replace 0 values with NaN

In medical datasets, zero often means "missing".

Columns affected:

Glucose

BloodPressure

SkinThickness

Insulin

BMI

✔ Step 2: Missing Value Handling

The project applies 3 different strategies:

Mean Imputation

Median Imputation

Mode Imputation

Each strategy trains its own KNN model.

📊 Exploratory Data Analysis

The project includes:

Shape + head of dataset

Missing value count

Data types

Statistical summary

Heatmap of feature correlations

Target distribution countplot

Histograms of all features

🤖 Model Training (KNN)

For each imputation strategy:

Features are standardized

Train-test split with stratification

KNN tested for k = 1 to 15

Best K selected

Model evaluated using:

Accuracy

Confusion Matrix

Classification Report

🎯 PCA Visualization

The model also reduces the dataset to 2 principal components (PC1 & PC2) and then:

Fits KNN on PCA-transformed data

Plots decision boundary

Uses separate color coding for:

Outcome 0 (No diabetes)

Outcome 1 (Diabetes)

📈 Output Plots

The project generates:

Correlation Heatmap

Target Distribution Plot

Histograms

Accuracy vs K line graph

PCA Decision Boundary (for each strategy)

▶️ How to Run

Install dependencies:

pip install pandas numpy matplotlib seaborn scikit-learn


Run the script:

python diabetes_knn.py

🏁 Conclusion

This project demonstrates how imputing missing data with different strategies impacts model performance. PCA-based visualization helps interpret how KNN separates the two classes in reduced dimensional space.

You now have a complete Machine Learning workflow that covers:

✔ Data cleaning
✔ Missing value handling
✔ EDA
✔ KNN modeling
✔ Hyperparameter tuning
✔ PCA visualization
