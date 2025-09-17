# House Prices Prediction – Kaggle Competition

This project was developed as part of the Econometrics course in my Master’s in Data Science.
The objective is to predict housing prices based on multiple socioeconomic and geographic features, using advanced regression and machine learning techniques.

---
## 📊 Methods
- **Exploratory Data Analysis (EDA):** distribution analysis, correlations, visualizations.
- **Feature Engineering:** ratios, logarithmic transformations, and interaction terms. 
- **Data Preprocessing:** missing value imputation, scaling, dummy encoding. 
- **Modeling:** predictive modeling with **XGBoost** and cross-validation. 
- **Evaluation:** feature importance, error metrics, and visualization of results. 
- **Predictions:** generation of final Kaggle submission file. 

## 🛠️ Tools & Libraries
- **Language:** R
- **Key packages:** xgboost, dplyr, caret, ggplot2, corrplot, skimr, DataExplorer, fastDummies, yardstick, workflows, recipes.

---
## 📂 Repository Structure
```
ds-house-prices-kaggle/
│
├── data/                # Training and test datasets (not included, download from Kaggle)
├── notebooks/           # Modular RMarkdown workflow
│   ├── 01-eda.Rmd       # Exploratory Data Analysis
│   ├── 02-feature-engineering.Rmd
│   ├── 03-model-training.Rmd
│   ├── 04-evaluation.Rmd
│   └── 05-final-predictions.Rmd
├── models/              # Saved models and feature importance tables
├── reports/             # Reports and results
│   └── figures/         # Visualizations and plots
├── .gitignore
└── README.md
```
---

## 🚀 How to Reproduce
1. Install the required R packages:
   ```R
   install.packages(c("xgboost","dplyr","fastDummies","caret","doParallel",
                      "tune","parsnip","recipes","dials","rsample","yardstick",
                      "workflows","tibble","DescTools","ggplot2","skimr","DataExplorer","corrplot"))```

2. Download the dataset from Kaggle:

   House Prices: Advanced Regression Techniques

3. Place train.csv and test.csv inside data/.

4. Run the notebook:
   ```R               
   rmarkdown::render("notebooks/01-eda.Rmd")
   rmarkdown::render("notebooks/02-feature-engineering.Rmd")
   rmarkdown::render("notebooks/03-model-training.Rmd")
   rmarkdown::render("notebooks/04-evaluation.Rmd")
   rmarkdown::render("notebooks/05-final-predictions.Rmd")
   ```

---
## 📈 Results
- RMSE on cross-validation: 24959.30203
- Feature importance analysis highlighted median_income, rooms_per_household, and geographic variables.

---

## 📑 Rendered Reports
- [Exploratory Data Analysis](reports/html/01-eda.nb.html)
- [Feature Engineering](reports/html/02-feature-engineering.nb.html)
- [Model Training](reports/html/03-model-training.nb.html)
- [Evaluation](reports/html/04-evaluation.nb.html)
- [Final Predictions](reports/html/05-final-predictions.nb.html)

---
## 📜 License
   MIT License
