# Boston House Price Prediction

A machine learning project that predicts median house prices in Boston suburbs using regression models built with Python and scikit-learn.

> **Note on the dataset:** The Boston Housing dataset contains a feature (`B`) derived from racial demographics and has been removed from scikit-learn for ethical reasons. This project uses it for learning purposes only and should not be used for real-world pricing decisions.

## Problem Statement

Given features of a Boston suburb (crime rate, number of rooms, distance to employment centres, etc.), predict the median home value (`MEDV`, in $1000s).

## Dataset

- **Source:** [add source link, e.g. the original StatLib / Kaggle page]
- **Rows:** 506
- **Features:** 13 input features + 1 target (`MEDV`)

| Feature | Description |
|---------|-------------|
| CRIM | Per-capita crime rate |
| RM | Average number of rooms per dwelling |
| LSTAT | % lower-status population |
| ... | [add the rest you actually use] |

## Approach

1. **Exploratory data analysis**: [summarize what you checked: missing values, distributions, correlations]
2. **Preprocessing**: [e.g. train/test split, feature scaling with StandardScaler]
3. **Models trained**: [e.g. Linear Regression, Ridge, Random Forest]
4. **Evaluation**: R² score, RMSE, MAE on the held-out test set

## Results

| Model | R² | RMSE |
|-------|----|------|
| [Model 1] | [value] | [value] |
| [Model 2] | [value] | [value] |

**Key takeaways:** [2 to 3 sentences: which features mattered most, which model won, what the limitations are]

## Project Structure

```
bostonhousepricing/
├── data/
│   └── boston.csv
├── notebooks/
│   └── boston_house_price_analysis.ipynb
├── regmodel.pkl
├── requirements.txt
├── LICENSE
└── README.md
```

## How to Run

```bash
# 1. Clone the repository
git clone https://github.com/Afrojkhan-glitch/bostonhousepricing.git
cd bostonhousepricing

# 2. Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Open the notebook
jupyter notebook notebooks/boston_house_price_analysis.ipynb
```

## Tech Stack

- Python
- pandas, NumPy
- scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

## Limitations and Future Work

- Small dataset (506 rows), so results may not generalize
- Dataset has known ethical issues (see note above)
- [ ] Try the California Housing dataset for comparison
- [ ] Add hyperparameter tuning
- [ ] Build and deploy a simple Streamlit app

## License

Distributed under the MIT License. See `LICENSE` for details.

## About Me
Hi there! I'm **Afroj Ahmad Khan**, an aspiring data analyst with a growing interest in data science and machine learning.
I enjoy building end-to-end projects, from cleaning data and writing SQL to training models and deploying them as web apps.
