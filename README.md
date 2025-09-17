# House Prices Prediction – Kaggle Competition

This project was developed as part of the Econometrics course in my Master’s in Data Science.  
The objective is to predict housing prices based on multiple socioeconomic and geographic features, using advanced regression and machine learning techniques.

## 📊 Methods
- Exploratory Data Analysis (EDA) with `ggplot2`, `skimr`, and `DataExplorer`.
- Feature engineering: ratios, logarithmic transformations, and interaction terms.
- Data preprocessing: missing value imputation, scaling, and dummy encoding.
- Predictive modeling with **XGBoost** and cross-validation.

## 🛠️ Tools & Libraries
R, XGBoost, dplyr, caret, ggplot2, corrplot, skimr, DataExplorer.

## 📂 Repository Structure
ds-house-prices-kaggle/
│
├── data/                # Training and test datasets (not included, download from Kaggle)
├── notebooks/           # Modular RMarkdown workflow
│   ├── 01-eda.Rmd               # Exploratory Data Analysis
│   ├── 02-feature-engineering.Rmd
│   ├── 03-model-training.Rmd
│   ├── 04-evaluation.Rmd
│   └── 05-final-predictions.Rmd
├── models/              # Saved models and feature importance tables
├── reports/             # Reports and results
│   └── figures/         # Visualizations and plots
├── .gitignore
└── README.md

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

## 📈 Results
- RMSE on cross-validation: 24959.30203
- Feature importance analysis highlighted median_income, rooms_per_household, and geographic variables.

## 📜 License
   MIT License
