# 🚗 Car Price Prediction

> A machine learning project that predicts used car prices using Linear Regression, backed by comprehensive Exploratory Data Analysis (EDA).

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## 📌 Project Overview

This project develops a predictive model to estimate the **market price of used cars** based on key vehicle attributes. Through rigorous Exploratory Data Analysis (EDA), the most influential features were identified and used to train a **Linear Regression** model that achieves an **R² of 0.83** — explaining 83% of the variance in car prices.

Whether you're a buyer, seller, or analyst, this model provides a data-driven baseline for fair used car valuation.

---

## ✨ Key Features

- 📊 **Comprehensive EDA** — Descriptive statistics, correlation heatmaps, pairplots, and categorical breakdowns
- 🔍 **Feature Importance Analysis** — Identifies `Year`, `Mileage`, and `Engine Size` as the strongest predictors
- 🤖 **Linear Regression Model** — Clean, interpretable, and well-evaluated
- 📈 **Performance Visualizations** — Predicted vs. actual price scatter plots and line plots
- 📁 **Well-Structured Notebook** — Step-by-step, reproducible analysis

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| **Python 3.8+** | Core programming language |
| **Jupyter Notebook** | Interactive development environment |
| **Pandas** | Data manipulation and analysis |
| **NumPy** | Numerical computing |
| **Matplotlib** | Data visualization |
| **Seaborn** | Statistical data visualization |
| **Scikit-Learn** | Machine learning (Linear Regression, metrics) |

---

## 🤖 Machine Learning Model

| Property | Detail |
|---|---|
| **Algorithm** | Linear Regression |
| **Library** | `scikit-learn` |
| **Input Features** | `Year`, `Engine Size`, `Mileage` |
| **Target Variable** | `Price` (USD) |

### Model Performance

| Metric | Value |
|---|---|
| **Mean Absolute Error (MAE)** | $1,703.98 |
| **Mean Squared Error (MSE)** | $4,520,798.58 |
| **Root Mean Squared Error (RMSE)** | ~$2,126.21 |
| **R-Squared (R²)** | **0.83** |

> The model explains **83%** of the variance in used car prices using only three numeric features — a strong result for a simple linear model.

---

## 📂 Dataset

The dataset contains used car listings with the following attributes:

| Column | Type | Description |
|---|---|---|
| `Price` | Numeric (Target) | Sale price of the car in USD |
| `Year` | Numeric | Year of manufacture |
| `Engine Size` | Numeric | Engine displacement in liters |
| `Mileage` | Numeric | Total distance traveled in miles |
| `Make` | Categorical | Car manufacturer (e.g., Ford, BMW, Audi, Honda) |
| `Model` | Categorical | Specific car model (e.g., Model A, B, C, D) |
| `Fuel Type` | Categorical | Fuel used (e.g., Petrol, Diesel, Electric) |
| `Transmission` | Categorical | Transmission type (e.g., Automatic, Manual) |

### Key EDA Insights

- ✅ **No missing values** — the dataset is clean and well-structured
- 📈 **Year vs Price** — Strong positive correlation (r = **0.85**); newer cars cost significantly more
- 📉 **Mileage vs Price** — Strong negative correlation (r = **−0.65**); higher mileage reduces value
- 🔧 **Engine Size vs Price** — Moderate positive correlation (r = **0.45**)
- ⚖️ **Balanced categories** — Even distribution across `Make`, `Model`, `Fuel Type`, and `Transmission`

---

## 📦 Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Jupyter Notebook or JupyterLab

### Setup

1. **Clone the repository:**

   ```bash
   git clone https://github.com/aditya97-bot/project_.git
   cd project_
   ```

2. **Create a virtual environment (recommended):**

   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # macOS / Linux
   source venv/bin/activate
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

---

## 📋 Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

Install all at once:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

---

## ▶️ How to Run

1. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

2. Open the file:

   ```
   car price predictor.ipynb
   ```

3. Run all cells sequentially using **Kernel → Restart & Run All**

The notebook is fully self-contained and will:
- Load and explore the dataset
- Generate all EDA visualizations
- Train the Linear Regression model
- Evaluate and visualize predictions

---

## 📁 Project Structure

```
project_/
│
├── car price predictor.ipynb          # Main Jupyter notebook
│
├── 📊 EDA Visualizations
│   ├── barplot data info.png          # Bar plots of categorical features
│   ├── descriptive statistics of car prices.png  # Summary statistics chart
│   ├── Heatmap data info.png          # Correlation heatmap
│   ├── lineplot data info.png         # Line plot of price trends
│   ├── pairplot data info.png         # Feature pair plots
│   ├── swarmplot data info.png        # Swarm plot distributions
│   ├── predicted and actual data.png  # Model prediction vs actual
│
├── 📊 Feature Visualizations
│   ├── engine size.png                # Engine size distribution
│   ├── fuel type.png                  # Fuel type distribution
│   ├── make.png                       # Car make distribution
│   ├── mileage.png                    # Mileage distribution
│   ├── model.png                      # Car model distribution
│   ├── price.png                      # Price distribution
│   ├── transmission.png               # Transmission type distribution
│   ├── year.png                       # Year distribution
│
├── README.md                          # Project documentation
├── CONTRIBUTING.md                    # Contribution guidelines
└── LICENSE                            # MIT License
```

---

## 📸 Screenshots

### Correlation Heatmap
![Heatmap](Heatmap%20data%20info.png)

### Predicted vs Actual Prices
![Predicted vs Actual](predicted%20and%20actual%20data.png)

### Pair Plot — Feature Relationships
![Pairplot](pairplot%20data%20info.png)

---

## 🚀 Future Improvements

- [ ] **Encode categorical features** (`Make`, `Model`, `Fuel Type`, `Transmission`) using one-hot encoding to improve accuracy
- [ ] **Feature engineering** — Add interaction terms (e.g., `Year × Mileage`)
- [ ] **Advanced models** — Test Random Forest, Gradient Boosting (XGBoost, LightGBM)
- [ ] **Hyperparameter tuning** — Use GridSearchCV or Optuna for optimization
- [ ] **Cross-validation** — Implement k-fold CV for more robust evaluation
- [ ] **Web application** — Build a Flask/Streamlit UI for real-time price prediction
- [ ] **Dataset expansion** — Include more car makes, regions, and years

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🔗 Repository Information

```bash
git clone https://github.com/aditya97-bot/project_.git
```

| | |
|---|---|
| **Repository** | [github.com/aditya97-bot/project_](https://github.com/aditya97-bot/project_) |
| **Language** | Python |
| **License** | MIT |

---

*Built with ❤️ and data science.*
