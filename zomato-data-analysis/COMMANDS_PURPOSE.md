# 📚 Commands Used in Zomato EDA

## 📦 Setup & Loading

| Command                                         | Purpose                                       |
| ----------------------------------------------- | --------------------------------------------- |
| `import numpy as np`                            | Import NumPy library                          |
| `import pandas as pd`                           | Import Pandas library                         |
| `import seaborn as sns`                         | Import Seaborn library                        |
| `import matplotlib.pyplot as plt`               | Import Matplotlib                             |
| `%matplotlib inline`                            | Show plots inside Jupyter notebook            |
| `plt.rcParams['figure.figsize'] = (12,6)`       | Set default figure size for all plots         |
| `pd.read_csv("zomato.csv", encoding='latin-1')` | Load CSV file with special character encoding |
| `pd.read_excel("Country-Code.xlsx")`            | Load Excel file                               |

---

## 🔍 Data Inspection

| Command             | Purpose                                     |
| ------------------- | ------------------------------------------- |
| `df.head()`         | Show first 5 rows                           |
| `df.columns`        | Show all column names                       |
| `df.info()`         | Show data types, null counts, memory usage  |
| `df.describe()`     | Show statistical summary of numeric columns |
| `df.dtypes`         | Show data type of each column               |
| `df.isnull().sum()` | Count missing values per column             |

---

## 🔗 Merging Data

| Command                                                   | Purpose                                                       |
| --------------------------------------------------------- | ------------------------------------------------------------- |
| `pd.merge(df, df_country, on='Country Code', how='left')` | Merge Zomato data with Country Code file to get country names |

---

## 📊 Grouping & Aggregation

| Command                                                                      | Purpose                                                   |
| ---------------------------------------------------------------------------- | --------------------------------------------------------- |
| `final_df.groupby(['Aggregate rating','Rating color','Rating text']).size()` | Group by multiple columns and count records in each group |
| `final_df.groupby(...).size().reset_index()`                                 | Same as above but convert result to DataFrame             |
| `final_df.Cuisines.value_counts().head(10).reset_index()`                    | Find top 10 most common cuisines                          |

---

## 🌍 Filtering & Analysis

| Command                                    | Purpose                       |
| ------------------------------------------ | ----------------------------- |
| `final_df[final_df['Country'] == 'India']` | Filter rows for India only    |
| `final_df['Country'].value_counts()`       | Count restaurants per country |

---

## 📈 Visualization

| Command                                                                   | Purpose                                |
| ------------------------------------------------------------------------- | -------------------------------------- |
| `sns.heatmap(df.isnull(), yticklabels=False, cbar=False, cmap="viridis")` | Visualize missing values as heatmap    |
| `sns.countplot(x='Rating color', data=final_df, palette=...)`             | Bar chart of rating color distribution |
| `plt.pie(city_values[:5], labels=city_labels[:5], autopct='%1.1f%%')`     | Pie chart of top 5 cities              |
