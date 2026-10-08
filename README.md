# Boston House Price Prediction

A machine learning project that predicts median house prices in Boston suburbs using regression models built with Python and scikit-learn. The trained model is saved with pickle for reuse.

> **Note on the dataset:** The Boston Housing dataset contains a feature (`B`) derived from racial demographics, and it has been removed from scikit-learn for ethical reasons. This project uses it for learning purposes only. It should not be used for real-world pricing decisions.

## Problem Statement

Given features of a Boston suburb, such as crime rate, average number of rooms, and distance to employment centres, predict the median home value (`MEDV`, in $1000s).

## Dataset

- **Source:** [CHANGE THIS: paste the link where you got boston.csv, e.g. Kaggle]
- **Rows:** 506
- **Features:** 13 input features and 1 target (`MEDV`)
- **File:** `data/boston.csv`

| Feature | Description |
|---------|-------------|
| CRIM | Per-capita crime rate by town |
| ZN | Proportion of residential land zoned for large lots |
| INDUS | Proportion of non-retail business acres per town |
| CHAS | Charles River dummy variable (1 if tract bounds river) |
| NOX | Nitric oxide concentration |
| RM | Average number of rooms per dwelling |
| AGE | Proportion of owner-occupied units built before 1940 |
| DIS | Weighted distance to five Boston employment centres |
| RAD | Index of accessibility to radial highways |
| TAX | Property-tax rate per $10,000 |
| PTRATIO | Pupil-teacher ratio by town |
| B | Demographic feature (see ethical note above) |
| LSTAT | Percentage of lower-status population |
| MEDV | **Target:** median home value in $1000s |

## Approach

1. **Data loading and inspection:** loaded the CSV with pandas and checked its shape, data types, and missing values.
2. **Exploratory data analysis:** examined feature distributions and correlations with the target.
3. **Preprocessing:** split the data into training and test sets and prepared the features for modelling.
4. **Model training:** trained [CHANGE THIS: e.g. Linear Regression] on the training set.
5. **Evaluation:** measured performance on the held-out test set using R² score and error metrics.
6. **Model saving:** saved the trained model as `regmodel.pkl` using pickle.

## Results

| Model | R² Score |
|-------|----------|------|
| [Linear Regression] | [0.7112260057484932] |

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

# 4. Launch the notebook
jupyter notebook notebooks/boston_house_price_analysis.ipynb
```

Run the cells from top to bottom. The notebook reads the data from `data/boston.csv`.

## Using the Saved Model

```python
import pickle

with open("regmodel.pkl", "rb") as f:
    model = pickle.load(f)

# Pass a 2D array of the 13 features, in the same order and scaling used in training
# prediction = model.predict(new_data)
```

> The model was trained with a specific scikit-learn version. If loading fails, install the version listed in `requirements.txt`.

## Tech Stack

- Python
- pandas and NumPy
- scikit-learn
- Matplotlib and Seaborn
- Jupyter Notebook

## Limitations

- Small dataset (506 rows), so results may not generalise to other cities or years
- The data is old and reflects a specific place and time
- The dataset contains an ethically problematic feature (see note above)
- Only [CHANGE THIS: number] model(s) tested; no hyperparameter tuning

## Future Improvements

- [ ] Compare more models (Ridge, Lasso, Random Forest, Gradient Boosting)
- [ ] Add cross-validation and hyperparameter tuning
- [ ] Repeat the project with the California Housing dataset
- [ ] Build and deploy a simple web app (for example with Streamlit)

## License

Distributed under the MIT License. See `LICENSE` for details.

## About Me
Hi there! I'm **Afroj Ahmad Khan**, an aspiring data analyst with a growing interest in data science and machine learning.
I enjoy building end-to-end projects, from cleaning data and writing SQL to training models and deploying them as web apps.
