# 📊 Movie Revenue Prediction & Insights Dashboard

## 🔹 Project Overview

This project analyzes the **TMDB movie dataset** to explore factors influencing box office revenue and builds predictive models.

Key highlights:

* **EDA (Exploratory Data Analysis):** Trends in budget, revenue, popularity, and runtime.
* **Visualizations:** Interactive dashboards with Plotly + static plots with Matplotlib/Seaborn.
* **Machine Learning Models:** Linear Regression & Random Forest Regressor to predict movie revenue.
* **Insights Dashboard:** Feature importance analysis, revenue distributions, and movie rankings.

Dataset used:
`C:\Users\DEVASISH\Downloads\data\tmdb_5000_movies.csv` (from Kaggle/TMDB).

---

## 🔹 Features Implemented

1. **Data Cleaning & Preprocessing**

   * Removed rows with missing/zero budgets and revenues.
   * Extracted numeric features: `budget`, `popularity`, `runtime`, `vote_average`, `vote_count`.

2. **Exploratory Data Analysis**

   * Distribution of revenue and budget.
   * Correlation heatmap of numeric features.
   * Top 20 movies by revenue.
   * Relationships: Budget vs Revenue, Runtime vs Revenue.

3. **Visualization**

   * Matplotlib/Seaborn for static plots.
   * Plotly for interactive dashboards.

4. **Predictive Models**

   * **Linear Regression:**

     * R² \~ low (struggles with skewed data).
   * **Random Forest Regressor:**

     * Better performance, captures non-linear relationships.

5. **Insights**

   * Budget and vote count are the most important predictors.
   * Higher budgets don’t always guarantee high revenue (many outliers).
   * Popularity correlates with revenue but not strongly.

---

## 🔹 Installation & Setup

1. Clone or download the project.

2. Install required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn plotly scikit-learn
   ```

   (If using Anaconda, most are pre-installed. For Plotly interactive use: `conda install -c conda-forge ipywidgets`).

3. Open the Jupyter Notebook:

   ```bash
   jupyter notebook Movie_Revenue_Prediction.ipynb
   ```

---

## 🔹 How to Run

1. Load the dataset:

   ```python
   df = pd.read_csv("C:/Users/DEVASISH/Downloads/data/tmdb_5000_movies.csv")
   ```
2. Run each cell in the notebook step by step.
3. Visualizations will appear inline (Matplotlib) or interactive (Plotly).
4. Models will train and display performance metrics.

---

## 🔹 Results

* Random Forest outperforms Linear Regression on revenue prediction.
* Budget & vote count are the strongest predictors of revenue.
* EDA revealed that some movies with **moderate budgets but high popularity** achieved significant revenues.

---

## 🔹 Future Work

* Extract more features (genres, director, cast) from JSON fields.
* Try advanced models (XGBoost, Gradient Boosting).
* Deploy as a web app dashboard (Streamlit/Dash).

---

## 🔹 File Structure

```
📁 Movie-Revenue-Prediction
│── Movie_Revenue_Prediction.ipynb   # Jupyter Notebook (main project)
│── README.md                        # Project documentation
│── tmdb_5000_movies.csv             # Dataset (not uploaded if large)
```
## 📌 Final Output – Project Summary

* ✅ **Exploratory Data Analysis (EDA):**

  * Revenue distribution is highly skewed, with a few blockbuster movies earning exceptionally high revenue.
  * **Budget vs Revenue** shows a positive trend but with many outliers (big budgets don’t always mean success).
  * **Correlation Analysis** shows that `budget`, `vote_count`, and `popularity` are most related to revenue.

* ✅ **Top Insights:**

  * Top-grossing movies (e.g., Avatar, Titanic) dominate revenue despite being relatively few.
  * Movies with moderate budgets but strong popularity sometimes perform better than high-budget flops.
  * Runtime has little impact on revenue beyond a certain range.

* ✅ **Machine Learning Models:**

  * **Linear Regression** → Poor fit due to skewed, non-linear relationships.
  * **Random Forest Regressor** → Significantly better performance, able to capture complex patterns.
  * **Feature Importance:** Budget and Vote Count emerged as the strongest predictors of revenue.

* ✅ **Dashboard Visualizations:**

  * Interactive charts for Budget vs Revenue, Runtime vs Revenue, and Feature Importance.
  * Bar chart of Top 20 movies by revenue.

### 🎯 Conclusion

This project successfully demonstrated how **data science techniques** (EDA + ML models) can be applied to understand and predict movie revenues.
While the dataset is limited in scope (only numeric features used), results highlight that **budget + audience engagement (votes, popularity)** are strong drivers of revenue. With additional features like **genres, cast, and director**, model accuracy could improve further.
