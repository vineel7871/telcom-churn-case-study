# Telecom Churn Case Study

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📋 Overview

This project analyzes customer churn in the telecom industry using machine learning techniques. The analysis focuses on identifying high-value customers who are at risk of churning and building predictive models to help reduce customer attrition.

## 🎯 Business Problem

In the telecom industry, customers can choose from multiple service providers and actively switch from one operator to another. The telecommunications industry experiences an average churn rate of 15-25% annually. Given that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has become even more important than customer acquisition.

**Key Objectives:**
- Analyze customer-level data to identify patterns that indicate churn
- Build predictive models to identify high-value customers at risk of churning
- Identify key indicators of churn to help reduce customer attrition

## 📊 Dataset

The dataset contains customer usage patterns across 4 months (June, July, August, September):
- **Total Records:** ~99,000 customers
- **Features:** 226 columns including call details, recharge information, data usage, etc.
- **Churn Rate:** ~8.5% among high-value customers
- **File Size:** 75MB

> 📖 A detailed **Data Dictionary** (`Data Dictionary- Telecom Churn Case Study.xlsx`) is included in the repository that explains all features.

### Key Feature Categories:
- Revenue/ARPU (Average Revenue Per User)
- Voice usage (local, STD, roaming)
- Data usage (2G/3G volumes)
- Recharge patterns (amount, frequency)
- Service usage indicators

## 🔍 Analysis Approach

### 1. Data Preprocessing
- Removed redundant columns (IDs, dates, single-value columns)
- Handled missing values strategically
- Feature engineering based on domain knowledge
- Filtered for high-value customers (70th percentile by ARPU)

### 2. Exploratory Data Analysis
- Analyzed churn patterns and distributions
- Examined correlations between features
- Identified key behavioral indicators

### 3. Dimensionality Reduction
- Applied PCA (Principal Component Analysis)
- Reduced features to 70 components explaining ~95% variance
- Combined with categorical features for modeling

### 4. Model Building

#### Models Implemented:
1. **Logistic Regression** (Baseline)
   - L1 regularization
   - Class weight balancing
   
2. **XGBoost Classifier**
   - Baseline model
   - Hyperparameter tuning using GridSearchCV
   - Final optimized model

### 5. Evaluation Metrics
- Precision, Recall, F1-Score
- ROC-AUC Score
- Confusion Matrix
- Focus on identifying churners (recall optimization)

## 📁 Repository Structure

```
telcom-churn-case-study/
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
├── Telecom Churn Case Study V4.ipynb                        # Main analysis notebook
├── Telecom Case Study XGBoost Tuning.ipynb                  # XGBoost hyperparameter tuning
├── telecom_churn_data.csv                                   # Dataset (75MB)
└── Data Dictionary- Telecom Churn Case Study.xlsx           # Feature descriptions
```

## 🚀 Getting Started

### Prerequisites

```bash
Python 3.7+
```

### Required Libraries

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/vineel7871/telcom-churn-case-study.git
cd telcom-churn-case-study
```

2. Install required packages:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

3. Open the Jupyter notebooks:
```bash
jupyter notebook
```

## 📓 Notebooks

### 1. Telecom Churn Case Study V4.ipynb
The main analysis notebook containing:
- Complete data preprocessing pipeline
- Exploratory data analysis
- Feature engineering
- Model building and evaluation
- Logistic Regression implementation

### 2. Telecom Case Study XGBoost Tuning.ipynb
Focused on XGBoost optimization:
- Baseline XGBoost model
- Hyperparameter tuning with GridSearchCV
- Model performance comparison
- Final optimized model

## 🔑 Key Findings

- High-value customers show distinct usage patterns before churning
- Recharge behavior and data usage are strong indicators
- PCA effectively reduced dimensionality while retaining predictive power
- XGBoost with tuned hyperparameters achieved optimal performance

## 📈 Results

The models successfully identify customers at risk of churn with performance metrics optimized for recall (to minimize false negatives in churn prediction).

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## 📝 License

This project is available for educational and research purposes. See the [LICENSE](LICENSE) file for details.

---

## 📞 Contact & Support

If you have any questions or suggestions, feel free to:
- Open an issue
- Submit a pull request
- Connect on LinkedIn (if applicable)

## 👤 Author

**Vineel**
- GitHub: [@vineel7871](https://github.com/vineel7871)

## 🙏 Acknowledgments

- Dataset source: Telecom industry customer behavior data
- Machine learning frameworks: scikit-learn, XGBoost

---

⭐ Star this repository if you find it helpful!
