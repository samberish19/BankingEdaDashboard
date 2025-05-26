# 📊 Banking EDA Dashboard

An interactive **Exploratory Data Analysis (EDA)** and **Power BI Dashboard** project built using **Python (Pandas, Seaborn, Matplotlib)** and **Power BI** to analyze customer banking data. The goal is to derive meaningful insights from the dataset and present them visually to support business decisions.

---

## 🚀 Project Overview

This project aims to:

- Clean and analyze banking customer data using Python.
- Perform statistical and visual EDA to uncover trends.
- Build a Power BI dashboard for effective decision support.
- Identify patterns in demographics, financial behavior, and product usage.

---

## 🧠 Key Objectives

- Understand customer segmentation by age, gender, marital status, etc.
- Analyze account balances, loan status, and income relationships.
- Visualize key metrics using Power BI for stakeholders.
- Detect high-value customers and potential risk groups.

---

## 🛠️ Tools & Technologies Used

| Tool/Library     | Description |
|------------------|-------------|
| Python           | Core language for data analysis |
| Pandas           | Data manipulation and preprocessing |
| Seaborn & Matplotlib | Visualization libraries for plots |
| Jupyter Notebook | Interactive development environment |
| Power BI         | Dashboard creation and storytelling |
| Excel/CSV        | Dataset formats |

---

## 📁 Project Structure

```
BankingEdaDashboard/
├── Banking.csv               # Raw dataset
├── Banking.xlsx              # Excel version of the dataset
├── BankingProject.ipynb      # Jupyter Notebook with full EDA
├── Banking Dashboard.pbix    # Interactive Power BI dashboard
└── README.md                 # Project documentation (this file)
```

---

## 📊 Dataset Description

Key columns in the dataset:

| Column              | Description |
|---------------------|-------------|
| Customer_ID         | Unique ID of customer |
| Age                 | Age in years |
| Gender              | Male/Female |
| Marital_Status      | Single, Married, etc. |
| Account_Type        | Savings, Current, etc. |
| Account_Balance     | Current balance in bank account |
| Loan_Status         | Indicates if customer has loan |
| Transaction_History | Recent transaction patterns |
| Income              | Monthly or annual income |
| Region              | Branch or geographic region |
| Tenure              | Duration with the bank |

---

## 📈 EDA in Python

### 1. Data Cleaning
- Null value handling
- Data type conversions
- Outlier detection and handling
- Dropping irrelevant features

### 2. Descriptive Statistics
- `.describe()`, `.value_counts()`
- Frequency tables
- Summary of numerical and categorical features

### 3. Univariate & Bivariate Analysis
- **Histograms**: Age, Income, Balance
- **Boxplots**: Gender vs Balance, Account Type vs Balance
- **Heatmap**: Feature correlation matrix
- **Countplots**: Gender, Marital Status, Account Type

### 4. Feature Engineering
- High-value customer flags
- Derived columns for tenure buckets or risk level
- Income groups and customer segments

### 5. Key Python Libraries
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

---

## 📉 Power BI Dashboard Highlights

The `.pbix` file includes:

- 📌 **KPI Cards** – Avg. Balance, Loan %age, Active Customers
- 📊 **Age Distribution** – Segmented by Gender & Region
- 🧮 **Balance vs. Income** – Scatter analysis
- 💰 **Loan Status Analysis** – Pie & bar charts
- 🏦 **Branch-Level Performance** – Comparative view by region
- 🔍 **Dynamic Filters** – Gender, Account Type, Loan, Region

### Power BI DAX Measures
```DAX
Avg_Balance = AVERAGE('Data'[Account_Balance])
Loan_Ratio = DIVIDE(CALCULATE(COUNTROWS('Data'), 'Data'[Loan_Status] = "Yes"), COUNTROWS('Data'))
```

---

## ✅ Key Insights

- Savings accounts dominate among customers aged 30-45.
- Male customers tend to have higher average balances.
- Long-tenured customers are more likely to hold loans.
- Branches in urban areas show higher customer retention.

---

## 🧪 How to Use This Project

### ▶️ For Jupyter Notebook
1. Clone the repo:
   ```bash
   git clone https://github.com/samberish19/BankingEdaDashboard.git
   cd BankingEdaDashboard
   ```
2. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn
   ```
3. Open the notebook:
   ```bash
   jupyter notebook BankingProject.ipynb
   ```

### ▶️ For Power BI
1. Download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
2. Open `Banking Dashboard.pbix`.

---

## 📬 Contact

- **GitHub**: [samberish19](https://github.com/samberish19)
- **Email**: your_email@example.com *(Replace with your actual email)*

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
