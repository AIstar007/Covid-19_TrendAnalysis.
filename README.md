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

Missing values in critical columns such as `Confirmed`, `Deaths`, or `Recovered` are handled using `SimpleImputer`:
   ```python
   from sklearn.impute import SimpleImputer

   imputer = SimpleImputer(strategy='mean')
   df[['Confirmed', 'Deaths', 'Recovered']] = imputer.fit_transform(df[['Confirmed', 'Deaths', 'Recovered']])
   ```

## 📈 Example Plot
   ```python
   import matplotlib.pyplot as plt

   # Plotting Confirmed cases trend for a specific country
   country_df = df[df['Country'] == 'India']
   plt.plot(country_df['Date'], country_df['Confirmed'], label='Confirmed')
   plt.xlabel('Date')
   plt.ylabel('Cases')
   plt.title('Covid-19 Trend in India')
   plt.legend()
   plt.show()
   ```

## 📌 Notes
- Ensure your dataset includes the following columns:
  ```css
  ['Country', 'Date', 'Confirmed', 'Deaths', 'Recovered']
- Convert the 'Date' column to datetime format:
  ```python
  df['Date'] = pd.to_datetime(df['Date'])

## 📃 License
This project is open-source and free to use under the **MIT License.**

## 🤝 Contributing
**Feel free to open issues or submit pull requests if you'd like to improve the analysis or add new features!**

