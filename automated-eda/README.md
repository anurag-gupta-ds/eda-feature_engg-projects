# 🤖 Automated Exploratory Data Analysis (EDA)

Automated Exploratory Data Analysis performed using YData Profiling and Sweetviz to generate comprehensive data profiling reports, identify data quality issues, analyze feature distributions, and gain insights into the dataset with minimal manual effort.

---

## 📌 Objective

To automatically analyze the dataset and generate detailed profiling reports containing:

* Dataset Overview
* Missing Value Analysis
* Duplicate Value Analysis
* Data Type Inspection
* Statistical Summaries
* Feature Distribution Analysis
* Correlation Analysis
* Data Quality Assessment
* Automated Visual Reports

---

## 🛠️ Tools & Libraries Used

* Python 3
* Pandas
* NumPy
* YData Profiling (`ydata-profiling`)
* Sweetviz
* Jupyter Notebook

---

## 📊 Analysis Performed

* Dataset Overview
* Data Type Analysis
* Missing Value Analysis
* Duplicate Value Analysis
* Statistical Summary Generation
* Feature Distribution Analysis
* Correlation Analysis
* Interaction Analysis
* Outlier Detection
* Automated Data Profiling Report Generation

---

## ⚙️ Data Preparation Performed

* Dataset Loading
* Data Inspection
* Data Quality Validation
* Missing Value Identification
* Duplicate Record Detection
* Feature Relationship Analysis
* Automated Feature Profiling

---

## 🔍 Key Insights

* Dataset structure and feature types were automatically identified.
* Missing values and data quality issues were detected.
* Numerical and categorical feature distributions were analyzed.
* Correlations between features were automatically generated.
* Potential outliers and anomalies were highlighted.
* Feature interactions were summarized through automated visualizations.
* Professional EDA reports were generated with minimal manual coding.

---

## 📈 Report Contents

* Overview Section
* Variables Summary
* Missing Values Report
* Duplicate Records Report
* Numerical Feature Analysis
* Categorical Feature Analysis
* Correlation Matrix
* Interactions Analysis
* Sample Data Preview
* Data Quality Warnings

---

## 🚀 What I Learned

* Automated Exploratory Data Analysis
* Data Profiling Techniques
* Dataset Quality Assessment
* Feature Distribution Analysis
* Correlation Analysis
* Identifying Missing Values and Duplicates
* Generating Professional Data Reports
* Understanding Dataset Characteristics Quickly
* Using YData Profiling and Sweetviz for Automated EDA

---

## 💻 Implementation

### YData Profiling

```python
from ydata_profiling import ProfileReport

profile = ProfileReport(
    df,
    title="Automated EDA Report",
    explorative=True
)

profile.to_file("ydata_report.html")
```

### Sweetviz

```python
import sweetviz as sv

report = sv.analyze(df)

report.show_html("sweetviz_report.html")
```

---

## 👨‍💻 Author

**Anurag Gupta**
