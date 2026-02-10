# Amazon Prime TV Shows and Movies - EDA & Regression Project  

## Project Overview  
This project analyzes a dataset of Amazon Prime TV shows and movies to build a regression model for predicting continuous target variables (e.g., IMDb scores) based on features like cast, director, genre, release year, runtime, and other metadata.  

The workflow includes:  
1. **Exploratory Data Analysis (EDA)** – Understanding data distribution, handling missing values, and visualizing key insights.  
2. **Data Preprocessing** – Merging datasets, cleaning, and feature engineering.  
3. **Modeling** – Implementing and comparing regression models:  
   - Linear Regression (baseline)  
   - Histogram-based Gradient Boosting Regressor  
   - XGBoost (final model)  
4. **Evaluation** – Performance measured using MSE, MAE, and R² scores.  
5. **Insights & Business Applications** – Identifying top contributors (actors/directors) and content strategy recommendations.  

---

## Dataset  
The dataset consists of two main files:  
- `credits_.csv` – Contains cast and crew details (person_id, name, role, character).  
- `titles_.csv` – Contains metadata for movies and TV shows (title, type, release_year, genres, IMDb/TMDB scores, etc.).  

After merging, the final dataset has **124,179 rows** and **19 columns**.  

---

## Data Cleaning & Preprocessing  
- Removed duplicate rows.  
- Handled missing values in columns like `seasons`, `age_certification`, `character`, `tmdb_score`, etc.  
- Merged `credits_` and `titles_` datasets on `id`.  
- Dropped irrelevant columns (`person_id`, `character`, `imdb_id`).  

---

## Exploratory Data Analysis (EDA)  
Key findings:  
- **Imbalanced dataset**: ~110,000 TV shows vs. ~10,000 movies.  
- **Top contributors**:  
  - Director: Joseph Kane  
  - Actor: George "Gabby" Hayes  
- **Visualizations**:  
  - Missing value percentages per column.  
  - Distribution of release years, genres, and ratings.  

---

## Machine Learning Models  
Three regression models were implemented and evaluated:  

| Model | MSE | MAE | R² |
|--------|-----|-----|-----|
| Linear Regression | 1.81 | 0.99 | 0.59 |
| Histogram-based Gradient Boosting | 3.15 | 1.45 | 0.28 |
| **XGBoost (Final Model)** | **1.81** | **0.99** | **0.59** |

- **XGBoost performed best** and was saved for future predictions.  
- Evaluation metrics were visualized using bar charts for clear comparison.  

---

## Key Insights  
1. **Content strategy**: Focus on top actors/directors to enhance viewer engagement.  
2. **Balancing content**: Address the imbalance between TV shows and movies.  
3. **Recommendation systems**: Use metadata (genres, cast, director) to improve suggestions.  
4. **Business growth**: Optimize content acquisition based on predictive scores.  

---

## Technologies Used  
- **Python** (Pandas, NumPy, Matplotlib, Seaborn)  
- **Machine Learning** (Scikit-learn, XGBoost)  
- **Jupyter Notebook**  
---
├── Sample_ML_Submission_Template.ipynb # Main Jupyter notebook
├── credits_.csv # Credits dataset
├── titles_.csv # Titles dataset
├── README.md # Project documentation
└── (optional) saved_model.pkl # Trained XGBoost model

---

## How to Run  
1. Clone the repository.  
2. Install required libraries:  
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost
---
Contact
Contributor: Mohd Osama
Feel free to reach out for questions or collaboration opportunities!

## 📁 Project Structure  
