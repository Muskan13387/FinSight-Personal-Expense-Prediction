# 💰 FinSight — Personal Expense Prediction

> **Can machine learning predict how much you will spend each month?**

FinSight is a **supervised machine learning regression project** designed to estimate a person's monthly expenses using financial and lifestyle factors such as **income, age, household size, rent, groceries, utilities, transportation, entertainment, and shopping**.

The project follows an **end-to-end machine learning workflow**, covering data preparation, exploratory data analysis, feature scaling, model training, hyperparameter tuning, and model evaluation.

---

## 🎯 Objectives

The main objectives of FinSight are to:

* 📊 Predict monthly personal expenses using machine learning.
* 🔎 Identify relationships between financial and lifestyle factors and monthly expenses.
* 🤖 Build a regularized regression model using **Ridge Regression**.
* ⚙️ Optimize model performance using **GridSearchCV**.
* 📈 Evaluate predictions using multiple regression metrics.
* 💾 Serialize the trained model using **Joblib** for future predictions.

---

## 🔄 Machine Learning Workflow

```text
Raw Dataset
     ↓
Data Preparation
     ↓
Exploratory Data Analysis
     ↓
Feature Selection
     ↓
Feature Scaling
     ↓
Train-Test Split
     ↓
Ridge Regression
     ↓
Hyperparameter Tuning
     ↓
GridSearchCV
     ↓
Model Evaluation
     ↓
Model Serialization
     ↓
Expense Prediction
```

---

## 📊 Dataset

The dataset contains financial and lifestyle information used to estimate monthly personal expenses.

### Dataset Features

| Feature           | Description                       |
| ----------------- | --------------------------------- |
| `age`             | Age of the individual             |
| `income`          | Monthly income                    |
| `household_size`  | Number of people in the household |
| `rent`            | Monthly rent                      |
| `utilities`       | Monthly utility expenses          |
| `groceries`       | Monthly grocery expenses          |
| `transportation`  | Transportation expenses           |
| `entertainment`   | Entertainment expenses            |
| `shopping`        | Shopping expenses                 |
| `monthly_expense` | 🎯 Target variable                |

### 🎯 Target Variable

**`monthly_expense`**

The model learns relationships between the available financial/lifestyle features and the individual's monthly expenses.

---

## 🔍 Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the dataset and identify patterns between financial factors and monthly expenses.

The analysis included:

* Understanding feature distributions
* Examining relationships between variables
* Correlation analysis
* Identifying potential patterns and trends
* Visualizing numerical features
* Exploring relationships with the target variable

---

## ⚙️ Data Preparation & Preprocessing

The dataset was prepared for machine learning through multiple preprocessing steps.

Key steps include:

* Data cleaning
* Feature selection
* Separating independent and dependent variables
* Train-test splitting
* Feature scaling
* Preparing data for regression modeling

Feature scaling was applied to ensure that variables with different numerical ranges could contribute appropriately to the model.

---

## 🤖 Machine Learning Model

### Ridge Regression

FinSight uses **Ridge Regression** as the primary regression algorithm.

Ridge Regression was selected because it introduces **L2 regularization**, which helps control model complexity and can be useful when predictor variables are correlated.

### Why Ridge Regression?

Financial variables such as income, rent, groceries, transportation, and shopping expenses can have relationships with each other.

Ridge Regression helps reduce the influence of large coefficients and can produce a more stable regression model.

---

## ⚙️ Hyperparameter Tuning

To optimize the Ridge Regression model, **GridSearchCV** was used.

The tuning process systematically evaluated different hyperparameter values and selected the configuration that produced the best model performance according to the chosen evaluation approach.

This helped improve the model beyond simply using default parameters.

---

## 📈 Model Evaluation

The regression model was evaluated using multiple performance metrics.

### Evaluation Metrics

* **R² Score** — measures the proportion of variance explained by the model.
* **Mean Absolute Error (MAE)** — measures the average absolute prediction error.
* **Mean Squared Error (MSE)** — measures the average squared prediction error.
* **Root Mean Squared Error (RMSE)** — measures prediction error in the same units as the target variable.

### 🏆 Model Performance

**R² Score: 97.8%**

The final Ridge Regression model achieved an **R² score of 0.978** on the evaluated data.

> **Note:** Model performance depends on the dataset, train-test split, preprocessing, and evaluation methodology.

---

## 💾 Model Serialization

The trained model was serialized using **Joblib**.

This allows the trained model to be saved and reused for making predictions without retraining it every time.

```python
import joblib

joblib.dump(model, "ridge_model.pkl")
```

The saved model can later be loaded and used for prediction:

```python
model = joblib.load("ridge_model.pkl")

prediction = model.predict(new_data)
```

---

## 🛠️ Technologies Used

### Programming Language

* Python

### Data Manipulation

* Pandas
* NumPy

### Data Visualization

* Matplotlib

### Machine Learning

* Scikit-learn
* Ridge Regression
* GridSearchCV

### Model Serialization

* Joblib

### Development Environment

* Jupyter Notebook

---

## 📁 Project Structure

```text
FinSight/
│
├── data/
│   └── dataset.csv
│
├── notebooks/
│   └── FinSight.ipynb
│
├── models/
│   └── ridge_model.pkl
│
├── requirements.txt
│
└── README.md
```

> Update the file/folder names above if your actual repository uses a different structure.

---

## 🧠 Key Takeaways

This project provided practical experience with:

* Supervised machine learning
* Regression problems
* Exploratory Data Analysis
* Feature selection
* Feature scaling
* Ridge Regression
* L2 regularization
* Hyperparameter tuning
* GridSearchCV
* Regression evaluation metrics
* Model serialization with Joblib
* Building an end-to-end ML workflow

---

## 🔮 Future Improvements

Potential improvements for FinSight include:

* 📊 Interactive expense dashboards
* 📅 Monthly and yearly expense trend analysis
* 💡 Personalized budgeting recommendations
* 🚨 Overspending alerts
* 📈 Expense forecasting
* 🤖 Comparison with additional regression algorithms
* 🔍 Explainable AI using SHAP
* 🌐 Deployment as an interactive web application
* 📱 Mobile-friendly financial insights

---

## 👩‍💻 Author

### Muskan Mulla

**Data Scientist | Machine Learning | Predictive Analytics**

📧 **Email:** [muskanmulla2311@gmail.com](mailto:muskanmulla2311@gmail.com)

💼 **LinkedIn:** https://www.linkedin.com/in/muskan-mulla-08a99b254/

💻 **GitHub:** https://github.com/Muskan13387

---

⭐ **If you found this project useful or interesting, consider giving the repository a star!**

