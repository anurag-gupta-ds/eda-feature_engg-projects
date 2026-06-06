## 🚢 Titanic Dataset Analysis — Commands & Purpose

---

## 📦 Setup & Loading

| Command | Purpose |
|---|---|
| `import numpy as np` | Import NumPy library |
| `import pandas as pd` | Import Pandas library |
| `import seaborn as sns` | Import Seaborn library |
| `import matplotlib.pyplot as plt` | Import Matplotlib library |
| `%matplotlib inline` | Show plots inside notebook |
| `pd.read_csv("train.csv")` | Load Titanic dataset |

---

## 🔍 Data Inspection (EDA)

| Command | Purpose |
|---|---|
| `df.head()` | Show first 5 rows |
| `df.shape` | Show rows and columns |
| `df.columns` | Show column names |
| `df.info()` | Show data types and null values |
| `df.describe()` | Statistical summary |
| `df.isnull().sum()` | Count missing values |
| `df.dtypes` | Show feature data types |

---

## 📊 Univariate Analysis

### ➤ Analysis on Single Feature

| Command | Purpose |
|---|---|
| `sns.countplot(x='Survived', data=df)` | Survival distribution |
| `sns.countplot(x='Sex', data=df)` | Male vs Female count |
| `sns.countplot(x='Pclass', data=df)` | Passenger class count |
| `sns.histplot(df['Age'])` | Age distribution |
| `sns.histplot(df['Fare'])` | Fare distribution |
| `sns.boxplot(x=df['Age'])` | Detect age outliers |
| `sns.boxplot(x=df['Fare'])` | Detect fare outliers |

---

## 📈 Bivariate Analysis

### ➤ Analysis Between Two Features

| Command | Purpose |
|---|---|
| `sns.barplot(x='Sex', y='Survived', data=df)` | Survival by gender |
| `sns.barplot(x='Pclass', y='Survived', data=df)` | Survival by passenger class |
| `sns.barplot(x='FamilySize', y='Survived', data=df)` | Survival vs family size |
| `sns.boxplot(x='Survived', y='Age', data=df)` | Age vs survival |
| `sns.boxplot(x='Pclass', y='Fare', data=df)` | Fare vs class |
| `sns.scatterplot(x='Age', y='Fare', data=df)` | Relationship between Age & Fare |

---

## 🧹 Missing Value Handling

| Command | Purpose |
|---|---|
| `df['Age'].fillna(df['Age'].median(), inplace=True)` | Fill missing Age values |
| `df['Embarked'].fillna(df['Embarked'].mode()[0], inplace=True)` | Fill missing Embarked values |
| `df.drop('Cabin', axis=1, inplace=True)` | Drop Cabin due to too many null values |

---

## 🧠 Feature Engineering

| Command | Purpose |
|---|---|
| `df['FamilySize'] = df['SibSp'] + df['Parch'] + 1` | Create total family size feature |
| `df['IsAlone'] = (df['FamilySize']==1).astype(int)` | Create IsAlone feature |
| `df['Title'] = df['Name'].str.extract(' ([A-Za-z]+)\.', expand=False)` | Extract title from Name |
| `df['Title'] = df['Title'].replace([...], 'Rare')` | Group rare titles |
| `df.drop(['Name','Ticket','PassengerId'], axis=1)` | Remove irrelevant features |

---

## 🔤 Encoding

| Command | Purpose |
|---|---|
| `df['Sex'] = df['Sex'].map({'male':0,'female':1})` | Encode gender |
| `pd.get_dummies(df, columns=['Embarked'], drop_first=True)` | One-hot encoding |
| `df['Title'] = df['Title'].map({...})` | Encode title categories |

---

## 🎯 Feature & Target Separation

| Command | Purpose |
|---|---|
| `X = df.drop('Survived', axis=1)` | Create feature matrix |
| `y = df['Survived']` | Create target variable |

---

## ✂️ Train-Test Split

| Command | Purpose |
|---|---|
| `train_test_split(X, y, test_size=0.33, random_state=42)` | Split dataset into train and test sets |

### Creates

- `X_train`
- `X_test`
- `y_train`
- `y_test`

---

## ⚖️ Feature Scaling

| Command | Purpose |
|---|---|
| `StandardScaler()` | Create scaling object |
| `scaler.fit_transform(X_train)` | Learn + scale training data |
| `scaler.transform(X_test)` | Scale testing data |

---

## 🤖 Model Training

| Command | Purpose |
|---|---|
| `from sklearn.linear_model import LogisticRegression` | Import model |
| `model = LogisticRegression()` | Create ML model |
| `model.fit(X_train, y_train)` | Train model |
| `model.predict(X_test)` | Predict output |
| `accuracy_score(y_test, y_pred)` | Check accuracy |

---

## 📌 Titanic Features & Recommended Plots

| Feature | Type | Best Plot | Purpose |
|---|---|---|---|
| `Age` | Numerical | Histogram / Boxplot | Distribution & outliers |
| `Fare` | Numerical | Histogram / Boxplot | Fare spread |
| `Sex` | Categorical | Countplot | Compare male/female |
| `Pclass` | Categorical | Countplot | Compare passenger classes |
| `Embarked` | Categorical | Countplot | Boarding port analysis |
| `Survived` | Binary Target | Countplot | Survival balance |
| `FamilySize` | Numerical | Barplot | Survival vs family size |
| `IsAlone` | Binary | Barplot | Alone vs non-alone |
| `Title` | Categorical | Countplot | Compare passenger titles |

---

## 🚀 ML Workflow Summary

```text
Load Dataset
    ↓
EDA
    ↓
Univariate Analysis
    ↓
Bivariate Analysis
    ↓
Multivariate Analysis
    ↓
Missing Value Handling
    ↓
Feature Engineering
    ↓
Encoding
    ↓
Feature Selection
    ↓
Create X and y
    ↓
Train-Test Split
    ↓
Feature Scaling
    ↓
Model Training
    ↓
Prediction & Accuracy
```

---
