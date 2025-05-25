# 🦠 Covid-19_TrendAnalysis

This project performs trend analysis on Covid-19 cases worldwide using Python. It helps in visualizing and understanding the progression of the pandemic using data visualization and preprocessing techniques.

---

## 🧰 Tools & Libraries Used

- `pandas`: For data loading, cleaning, and transformation.
- `numpy`: For efficient numerical operations.
- `matplotlib.pyplot`: For creating insightful visualizations.
- `sklearn.impute.SimpleImputer`: For handling missing values.

---

## 📊 Features

- 📅 Trend analysis by **Country** and **Date**
- 📈 Daily and cumulative charts for:
  - ✅ Confirmed cases
  - ⚰️ Deaths
  - 💚 Recoveries
- 🧹 Handling and imputation of missing values
- 🔄 Grouped aggregation using `pandas`
- 🧩 Customizable plots using `matplotlib`

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Covid-19_TrendAnalysis.git
   cd Covid-19_TrendAnalysis

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt

3. **Open the Jupyter Notebook**
   ```bash
   jupyter notebook covid_analysis.ipynb

## 🧹 Data Cleaning & Imputation

   Missing values in critical columns such as Confirmed, Deaths, or Recovered are handled using SimpleImputer:
   ```python
   from sklearn.impute import SimpleImputer
   imputer = SimpleImputer(strategy='mean')
   df[['Confirmed', 'Deaths', 'Recovered']] = imputer.fit_transform(df[['Confirmed', 'Deaths', 'Recovered']])

## 📈 Example Plot
