# -FIFA-World-Cup-2026-Prediction-Engine
# ⚽ FIFA World Cup 2026 Prediction Engine

A comprehensive Data Warehouse and Mining (DWM) project that utilizes historical international football data to predict match outcomes, scorelines, and team performance tiers for the upcoming 2026 World Cup.

## 🚀 Project Overview
This project implements a full machine learning pipeline in a Google Colab environment. It processes over **49,000 historical matches** and **333 unique teams** to provide data-driven insights.

### Key Features:
* **ETL Pipeline:** Automated extraction and transformation of raw CSV data.
* **Winner Prediction:** A **Gaussian Naïve Bayes** classifier to predict match winners based on historical matchups.
* **Scoreline Forecasting:** **Linear Regression** models to predict specific home and away scores.
* **Team Clustering:** **K-Means Clustering** to categorize teams into "Elite," "Mid-tier," and "Underdog" clusters based on scoring efficiency.

## 🛠️ Technical Stack
* **Language:** Python
* **Environment:** Google Colab / Jupyter Notebook
* **Libraries:** * `Pandas` & `NumPy` (Data Manipulation)
    * `Scikit-Learn` (Machine Learning Algorithms)
    * `Seaborn` & `Matplotlib` (Data Visualization)

## 📊 Methodology

### 1. Data Pre-processing (ETL)
- **Extraction:** Loading raw historical match data (`results.csv`).
- **Transformation:** Label Encoding categorical team names into numerical codes for model compatibility.
- **Dimensional Mapping:** Ensuring consistency across home and away team feature sets.

### 2. Machine Learning Models
- **Classification:** Naïve Bayes achieved an accuracy of ~51% in predicting the specific 'Outcome' category.
- **Regression:** Used to predict the total goals and specific scorelines (e.g., predicting a 2-1 result for USA vs Canada).
- **Clustering:** K-Means used to group teams by their average goals scored per match.

## 📈 Visualizations
The project includes a **Confusion Matrix** heatmap to evaluate the classification model's performance and identify where the model is most/least accurate.

## 📖 How to Use
1. Upload `results.csv` to the Colab environment.
2. Run the ETL cells to encode the data.
3. Use the `predict_2026_winner("Team A", "Team B")` function to see a predicted match outcome.
4. Use `predict_scoreline("Team A", "Team B")` to see a predicted final score.
