# Tesla Stock Price Prediction using Machine Learning

A machine learning project that predicts Tesla (TSLA) stock price movement using historical data and multiple classification models.

##  Dataset

`Tesla.csv` — 1,692 rows of daily Tesla stock data from **June 2010** to present, with the following columns:

| Column | Description |
|--------|-------------|
| `Date` | Trading date |
| `Open` | Opening price (USD) |
| `High` | Daily high price (USD) |
| `Low` | Daily low price (USD) |
| `Close` | Closing price (USD) |
| `Volume` | Number of shares traded |
| `Adj Close` | Adjusted closing price |

##  Models Used

- **Logistic Regression**
- **Support Vector Machine (SVC)**
- **XGBoost Classifier**

##  Features Engineered

- Day, month, year extracted from date
- Quarter-end indicator (`is_quarter_end`)
- Price change and return features

##  Project Structure

```
tesla-stock-prediction/
├── Tesla.csv                    # Historical stock data
├── Stock_Price_Prediction.ipynb # Main notebook
├── requirements.txt             # Python dependencies
└── README.md                    # This file
```

##  Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/tesla-stock-prediction.git
cd tesla-stock-prediction
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the notebook

```bash
jupyter notebook Stock_Price_Prediction.ipynb
```

> **Note:** The notebook originally loads data from `/content/Tesla.csv` (Google Colab path). If running locally, update the path to `Tesla.csv`.

##  Requirements

See `requirements.txt` for the full list. Key libraries:

- `pandas`, `numpy` — data manipulation
- `matplotlib`, `seaborn` — visualization
- `scikit-learn` — ML models and preprocessing
- `xgboost` — gradient boosted classifier

##  Workflow

1. Load and explore the Tesla CSV data
2. Visualize price trends and feature distributions
3. Engineer new features (date parts, quarter-end flag)
4. Prepare target variable (price direction: up/down)
5. Train/test split and feature scaling
6. Train Logistic Regression, SVM, and XGBoost models
7. Evaluate and compare model accuracies

##  License

This project is open source and available under the [MIT License](LICENSE).
