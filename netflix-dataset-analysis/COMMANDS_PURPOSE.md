# 🎬 Netflix Dataset Analysis — Commands & Purpose

## 📦 Setup & Loading

| Command | Purpose |
|----------|----------|
| `import numpy as np` | Import NumPy library |
| `import pandas as pd` | Import Pandas library |
| `import seaborn as sns` | Import Seaborn library |
| `import matplotlib.pyplot as plt` | Import Matplotlib library |
| `%matplotlib inline` | Show plots inside notebook |
| `pd.read_csv('netflix_titles.csv')` | Load Netflix dataset |

---

## 🔍 Data Inspection (EDA)

| Command | Purpose |
|----------|----------|
| `df.head()` | Show first 5 rows |
| `df.shape` | Show rows and columns |
| `df.columns` | Show column names |
| `df.info()` | Show data types and null values |
| `df.describe()` | Statistical summary |
| `df.isnull().sum()` | Count missing values |
| `df.dtypes` | Show feature data types |
| `df.duplicated().sum()` | Check duplicate records |

---

## 🧹 Missing Value Handling

| Command | Purpose |
|----------|----------|
| `df['director'].fillna('Unknown')` | Fill missing director values |
| `df['cast'].fillna('Unknown')` | Fill missing cast values |
| `df['country'].fillna('Unknown')` | Fill missing country values |
| `df['rating'].fillna(df['rating'].mode()[0])` | Fill missing ratings |
| `df['date_added'].fillna('Unknown')` | Handle missing dates |
| `df['duration'].fillna('Unknown')` | Handle missing duration values |

---

## ⚙️ Feature Engineering

| Command | Purpose |
|----------|----------|
| `pd.to_datetime(df['date_added'])` | Convert to datetime format |
| `df['year_added']=df['date_added'].dt.year` | Extract year from date |
| `df['month_added']=df['date_added'].dt.month` | Extract month from date |
| `top_countries=df['country'].value_counts().head(10).index` | Select top countries |
| `top_directors=df['director'].value_counts().head(10).index` | Select top directors |
| `top_ratings=df['rating'].value_counts().head(5).index` | Select top ratings |

---

## 📊 Univariate Analysis

### ➤ Analysis on Single Feature

| Command | Purpose |
|----------|----------|
| `sns.countplot(x='type',data=df)` | Movies vs TV Shows |
| `sns.histplot(x='release_year',data=df)` | Release year distribution |
| `sns.countplot(x='rating',data=df)` | Rating distribution |
| `sns.countplot(x='country',data=df)` | Country distribution |
| `sns.countplot(x='listed_in',data=df)` | Genre distribution |
| `df['director'].value_counts().head(10)` | Top directors |
| `df['country'].value_counts().head(10)` | Top countries |

---

## 📈 Bivariate Analysis

### ➤ Analysis Between Two Features

| Command | Purpose |
|----------|----------|
| `sns.countplot(x='type',hue='rating',data=df)` | Type vs Rating |
| `sns.countplot(y='country',hue='type',data=filtered_df)` | Country vs Type |
| `sns.countplot(y='country',hue='rating',data=filtered_df)` | Country vs Rating |
| `sns.boxplot(x='type',y='release_year',data=df)` | Type vs Release Year |
| `sns.countplot(y='director',hue='type',data=filtered_df)` | Director vs Type |

---

## 📈 Date Analysis

| Command | Purpose |
|----------|----------|
| `df['date_added']=pd.to_datetime(df['date_added'])` | Convert date column |
| `df['year_added']=df['date_added'].dt.year` | Extract year |
| `sns.countplot(x='year_added',data=df)` | Content added per year |
| `plt.xticks(rotation=90)` | Rotate labels |

---

## 📊 Top Category Analysis

| Command | Purpose |
|----------|----------|
| `df['country'].value_counts().head(10)` | Top countries |
| `df['director'].value_counts().head(10)` | Top directors |
| `df['rating'].value_counts().head(10)` | Top ratings |
| `df['listed_in'].value_counts().head(10)` | Top genres |

---

## 📌 Netflix Features & Recommended Plots

| Feature | Type | Best Plot | Purpose |
|----------|----------|----------|----------|
| type | Categorical | Countplot | Movies vs TV Shows |
| country | Categorical | Countplot | Country contribution |
| rating | Categorical | Countplot | Rating analysis |
| director | Categorical | Top 10 Countplot | Director analysis |
| listed_in | Categorical | Top 10 Countplot | Genre analysis |
| release_year | Numerical | Histogram | Release trend |
| year_added | Numerical | Countplot | Netflix growth |
| duration | Categorical | Countplot | Duration distribution |

---

## 🚀 EDA Workflow Summary

Load Dataset
    ↓
Data Inspection
    ↓
Missing Value Analysis
    ↓
Null Value Handling
    ↓
Duplicate Check
    ↓
Feature Engineering
    ↓
Univariate Analysis
    ↓
Bivariate Analysis
    ↓
Top Categories Analysis
    ↓
Date Analysis
    ↓
Business Insights
    ↓
Final Observations
