# Boston House Price Prediction

Welcome to the **Boston House Price Prediction** project! 🏠
This project builds a machine learning regression model that predicts the median value of houses in Boston neighbourhoods from 13 housing and neighbourhood features. It is a portfolio project that covers data cleaning, exploratory analysis, model training and evaluation.

---

## Project Requirements

### 1. Data Analysis (Data Analytics)

#### Objectives
Explore the dataset to understand which neighbourhood factors are related to house prices.

#### Key Specifications
- **Data Source**: `boston.csv` in this repository, with 506 rows and 13 features.
- **Target**: House price (`MEDV`, median home value in $1000s).
- **Features**: CRIM, ZN, INDUS, CHAS, NOX, RM, AGE, DIS, RAD, TAX, PTRATIO, B, LSTAT.
- **Data Quality**: No missing values. The header was fixed on load and all columns were converted to numeric.
- **Findings**: Average number of rooms (RM) has a strong positive correlation with price (0.70), while PTRATIO (-0.51) and TAX (-0.47) are negatively correlated.

---

### 2. Machine Learning Model (Data Science)

#### Objectives
Train a regression model to predict house prices and evaluate how well it generalizes.

#### Key Specifications
- **Model**: [Linear Regression]
- **Evaluation**: [0.7112260057484932]
- **Saved Model**: `regmodel.pkl`

---

## Repository Structure
```
bostonhousepricing/
│
├── boston.csv           # Dataset
├── project1.ipynb       # Analysis and model training notebook
├── regmodel.pkl         # Trained model
├── requirements.txt     # Python dependencies
├── README.md            # Project overview
└── LICENSE              # License information
```

---

## How to Run
```bash
git clone https://github.com/Afrojkhan-glitch/bostonhousepricing.git
cd bostonhousepricing
pip install -r requirements.txt jupyter
jupyter notebook project1.ipynb
```

---

## Limitations
The Boston housing dataset contains a feature `B` that is based on the racial composition of neighbourhoods, and it has been removed from scikit-learn for ethical reasons. This project uses it only for learning and practice, and the model should not be used for real housing decisions.

---

## License
This project is licensed under the Apache-2.0 License. See the [LICENSE](LICENSE) file for details.

---

## About Me
Hi there! I'm **Afroj Ahmad Khan**, an aspiring data analyst with a growing interest in data science and machine learning.
I enjoy building end-to-end projects, from cleaning data and writing SQL to training models and deploying them as web apps.
