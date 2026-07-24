# 🎓 EduScore ML: Student Performance Prediction

## 🧠 Project Overview

EduScore ML is a machine learning regression project that predicts student performance using educational and lifestyle-related features.

The main goal of this project is to build a simple, interpretable, and accurate regression model that can estimate a student's `Performance Index` based on study habits, previous academic performance, sleep hours, extracurricular activity, and practice behavior.

Since the target variable is numerical, this project is a regression problem. The final model used in this project is Linear Regression. Because the model uses multiple input features, it is considered a Multiple Linear Regression model.

---

## 📊 Dataset Overview

The dataset contains student-related information and one numerical target column.

### 🧾 Input Features

- `Hours Studied`
- `Previous Scores`
- `Extracurricular Activities`
- `Sleep Hours`
- `Sample Question Papers Practiced`

### 🎯 Target Variable

- `Performance Index`

The `Performance Index` column represents the final performance score of each student.

---

## ❓ Problem Statement

The main question of this project is:

**Can we predict a student's performance index using study hours, previous scores, extracurricular activity, sleep hours, and sample question papers practiced?**

The goal is not only to train a model, but also to understand how these features are related to student performance.

---

## 🧹 Data Cleaning

Before training the model, the dataset was checked and cleaned.

The cleaning steps included:

- Checking dataset shape
- Checking column information
- Checking missing values
- Checking duplicate rows
- Removing duplicate records
- Encoding the categorical column

The categorical column `Extracurricular Activities` was converted into numerical values:

```python
Yes = 1
No = 0
```

This conversion was necessary because machine learning models work with numerical values.

---

## 🔍 Exploratory Data Analysis

Exploratory Data Analysis was performed to better understand the dataset.

The EDA section included:

- Dataset overview
- Missing value check
- Duplicate value check
- Statistical summary
- Correlation heatmap
- Relationship between features and the target variable

The correlation analysis helped show which features had stronger relationships with the `Performance Index`.

---

## 🏗️ Feature and Target Selection

The selected input features were:

```python
features = [
    "Hours Studied",
    "Previous Scores",
    "Extracurricular Activities",
    "Sleep Hours",
    "Sample Question Papers Practiced"
]
```

The target variable was:

```python
y = df["Performance Index"]
```

---

## ✂️ Train-Test Split

The dataset was divided into training and testing sets.

```python
test_size = 0.2
random_state = 42
```

The training data was used to train the model, while the testing data was used for final evaluation.

---

## 🤖 Model Training

The final model used in this project was:

```python
LinearRegression(fit_intercept=True)
```

Although the model is implemented using `LinearRegression()` in scikit-learn, it is considered a Multiple Linear Regression model because it uses several input features to predict one numerical target variable.

---

## 📈 Model Evaluation

The final model was evaluated using the following regression metrics:

| Metric | Score |
|---|---:|
| MAE | 1.65 |
| RMSE | 2.08 |
| R2 Score | 0.9884 |

### 📌 Evaluation Interpretation

- **MAE = 1.65** means the model's predictions are off by about 1.65 points on average.
- **RMSE = 2.08** shows that the overall prediction error is low.
- **R2 Score = 0.9884** means the model explains about 98.84% of the variation in student performance.

These results show that the model performed very well on the test data.

---

## 📉 Visualizations

The project includes useful visualizations to better understand the data and model performance.

The visualizations include:

- Correlation heatmap
- Actual vs Predicted plot
- Residual distribution plot

These plots help show how well the model predicts student performance and how small the prediction errors are.

---

## 🎮 Fun Little Prediction Demo

A small prediction example was added to show how the trained model can predict the performance index for a new student.

Example input:

```python
sample_student = pd.DataFrame({
    "Hours Studied": [7],
    "Previous Scores": [85],
    "Extracurricular Activities": [1],
    "Sleep Hours": [8],
    "Sample Question Papers Practiced": [5]
})

predicted_score = final_model.predict(sample_student)

print("Predicted Performance Index:", round(predicted_score[0], 2))
```

This example shows how the model can be used to predict a student's expected `Performance Index` based on new input values.

---

## 🧰 Tools and Libraries

This project was built using:

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 📌 Project Workflow

The project followed these main steps:

1. Import libraries
2. Load the dataset
3. Explore the data
4. Clean the dataset
5. Encode categorical values
6. Select features and target
7. Split data into train and test sets
8. Train the Multiple Linear Regression model
9. Evaluate the model
10. Visualize the results
11. Make a sample prediction

---

## ✅ Final Conclusion

In this project, a Multiple Linear Regression model was used to predict student performance based on several educational and lifestyle-related features.

The dataset was cleaned by removing duplicate records and converting the categorical feature `Extracurricular Activities` into numerical form. After that, the data was split into training and testing sets.

The final selected model was Linear Regression with `fit_intercept=True`. Since the model uses multiple input features such as previous scores, hours studied, sleep hours, extracurricular activities, and sample question papers practiced, it is considered a Multiple Linear Regression model.

The final model achieved the following results on the test data:

- MAE: 1.65
- RMSE: 2.08
- R2 Score: 0.9884

The R2 Score shows that the model explains about 98.84% of the variation in student performance. The MAE value shows that the model's predictions are off by about 1.65 points on average, and the RMSE value shows that the overall prediction error is about 2.08 points.

Overall, the final Multiple Linear Regression model performed very well on this dataset. The results show that the selected features have a strong relationship with student performance, and a simple regression model can make accurate predictions with small errors.

---

## 🚀 Repository Description

A machine learning regression project for predicting student performance using Multiple Linear Regression, data cleaning, EDA, model evaluation, and prediction visualization.
