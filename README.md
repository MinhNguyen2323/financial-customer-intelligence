# 📊 Financial Customer Intelligence | BI & Machine Learning

**Customer Analytics | Predictive Modeling | Business Intelligence | Python**

## 📌 Overview

Can financial transaction data reveal not only who a bank's most valuable customers are, but also who might be losing interest before they leave?

This project develops an **end-to-end customer intelligence framework** that transforms financial transaction records into actionable insights for customer segmentation, lifetime value forecasting, and early behavioral decline detection.

The solution integrates machine learning models with a **five-tab interactive Plotly Dash dashboard**, bridging predictive analytics and business decision-making.

**Core objectives:**
- Understand customer spending patterns through RFM segmentation.
- Forecast six-month Customer Lifetime Value (CLV).
- Identify early signals of declining customer engagement.
- Translate analytical findings into actionable retention and growth strategies.

## 🗂️ Dataset

The analysis uses approximately **1.04 million credit card transactions** from **136 customers**, covering 2010–2019.

| Data Source | Description |
|---|---|
| `transactions_data.csv` | Transaction amounts, timestamps, merchant categories, and errors |
| `users_data.csv` | Customer demographics, income, and credit information |
| `cards_data.csv` | Card characteristics, limits, and brands |
| `mcc_codes.json` | Merchant Category Code reference data |

Data preparation includes cleaning, merging, feature engineering, and constructing customer-level behavioral indicators.

## 🔍 Analytical Framework

### 1. Customer Segmentation

Applied **Recency, Frequency, Monetary (RFM)** analysis to identify five customer segments, including Champions, Loyal, Potential, Need Attention, and At Risk.

Tracked segment changes across six-month periods to understand customer engagement and potential retention opportunities.

### 2. Customer Lifetime Value Prediction

Developed an **XGBoost regression model** to estimate customer value over a six-month horizon.

Combined behavioral and financial characteristics with PCA and K-Means to identify customer groups with different value profiles.

### 3. Behavioral Decline Detection

Built a **Logistic Regression classifier** to identify customers exhibiting signs of declining transaction activity.

Explored changes in spending consistency, transaction frequency, and merchant category preferences to better understand early disengagement signals.

### 4. Business Intelligence Dashboard

Integrated descriptive and predictive analytics into an interactive **Plotly Dash** application supporting customer monitoring, risk exploration, and strategic decision-making.

## 📈 Model Performance

| Model / Method | Objective | Result |
|---|---|---|
| RFM Segmentation | Customer behavioral profiling | 5 segments |
| XGBoost Regression | Six-month CLV prediction | **R² = 0.8998**, MAE ≈ $2,067 |
| PCA + K-Means | Customer value-based clustering | 3 clusters |
| Logistic Regression | Behavioral decline prediction | **ROC-AUC = 0.80**, Recall = 69% |

These results demonstrate the potential of combining interpretable segmentation with predictive modeling to support customer-level decision-making.

## 💡 Key Business Insights

- **Early warning signals:** Increased spending volatility may precede customer disengagement, suggesting opportunities for earlier intervention.
- **Retention opportunities:** The *Need Attention* segment represents approximately **29% of customers**, with only **21% transitioning to Potential**, highlighting a priority group for retention analysis.
- **Decline patterns:** High Volatility (~30%), Fewer but Bigger Transactions (~16%), and Essential Shift (~13%) were the most frequently identified behavioral patterns.
- **Transaction friction:** Insufficient Balance accounted for approximately **60% of transaction errors**, with notable concentration among customers with weaker credit profiles.
- **Growth potential:** One high-income CLV cluster showed opportunities for deeper engagement and targeted value development.

**Business implication:** Customer value and customer risk should be analyzed together. High-value customers are not necessarily highly engaged, and behavioral changes may provide useful signals before traditional segmentation reveals a problem.

## 🖥️ Interactive Dashboard

The dashboard contains five analytical views:

| Dashboard | Focus |
|---|---|
| **Overview** | Transaction KPIs, trends, and merchant categories |
| **Behavior** | RFM segmentation, spending patterns, and geographic insights |
| **Risk & Customer** | Transaction errors, credit profiles, and demographics |
| **CLV Intelligence** | Predicted customer value, clustering, and priority customers |
| **Decline Analysis** | Behavioral deterioration, spending shifts, and retention signals |

The dashboard is designed to make complex analytical outputs accessible through interactive visualizations and business-oriented KPIs.

## ⚖️ Strengths & Limitations

**Strengths**
- End-to-end workflow connecting data engineering, machine learning, and BI.
- Combines customer value forecasting with behavioral risk identification.
- Uses interpretable segmentation alongside predictive models.
- Translates analytical outputs into actionable business hypotheses.

**Limitations**
- The dataset contains only 136 customers despite its large transaction volume, limiting customer-level generalizability.
- CLV predictions retain meaningful absolute error and should not be treated as exact financial forecasts.
- Behavioral decline is a proxy for disengagement, not necessarily confirmed customer churn.
- Business recommendations have not been validated through controlled interventions or live deployment.

## 🛠️ Tech Stack

`Python` · `Pandas` · `NumPy` · `Scikit-learn` · `XGBoost` · `Imbalanced-learn` · `Plotly Dash` · `Matplotlib` · `Seaborn` · `Jupyter Notebook`

## 📂 Repository Structure

```text
financial-customer-intelligence/
├── Financial Transactions.rar
├── preprocess+model.rar
├── my-dashboard.rar
├── Report.pdf
├── Slides.pdf
└── README.md
```

**Archive contents:**

- `Financial Transactions.rar`: Raw transaction, customer, card, and merchant category data.
- `preprocess+model.rar`: Data preprocessing and analytical notebooks covering RFM, CLV prediction, and behavioral decline modeling.
- `my-dashboard.rar`: Interactive Plotly Dash application source code.
- `Report.pdf`: Complete project documentation.
- `Slides.pdf`: Project presentation.

## 🚀 Getting Started

### 1. Download and extract the archives

Extract the three `.rar` files and organize the project into working directories for data, modeling, and dashboard development.

### 2. Install dependencies

```bash
pip install pandas numpy scikit-learn xgboost imbalanced-learn plotly dash dash-bootstrap-components scipy matplotlib seaborn joblib jupyter
```

**Suggested environment:** Python 3.8+ with at least 8 GB RAM.

### 3. Run the analytical pipeline

Inside the extracted `preprocess+model` directory, execute the notebooks in the following order:

1. `preprocess BI.ipynb`
2. `RFM.ipynb`
3. `BI-CLV.ipynb`
4. `Churn Analysis & Prediction.ipynb`

Check and update local file paths as needed before execution.

### 4. Launch the dashboard

From the extracted dashboard source directory:

```bash
python app.py
```

Open `http://127.0.0.1:8050` in your browser.

*Note: Initial loading may take additional time due to transaction-level data aggregation.*

## 🎓 Academic Context

- **Course:** Intelligent Management Support Systems
- **Institution:** University of Economics Ho Chi Minh City (UEH)
- **Faculty:** Business Information Technology
- **Project Type:** Five-member collaborative academic project
- **Focus:** Financial Analytics, Customer Intelligence, and Decision Support

*Beyond predicting customer behavior, this project explores a question I find particularly interesting: how can data help us understand the decisions people make, recognize meaningful changes, and respond more intelligently?*
