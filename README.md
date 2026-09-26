##Diabetes Risk Factor Preprocessing

Exploratory data cleaning and preprocessing on a clinical dataset of 520 patients, examining early-stage symptom indicators of diabetes (polyuria, polydipsia, sudden weight loss, and 13 other features) alongside patient age and gender.

This project was built while learning data preprocessing fundamentals in pandas — handling missing values, encoding categorical features, and inspecting feature distributions before modeling.

Dataset

520 patient records with 16 symptom-related features (mostly binary: present/absent) plus age, gender, and a binary class label (positive/negative for diabetes risk).

Add the dataset source/citation here, e.g. the UCI "Early Stage Diabetes Risk Prediction" dataset, or wherever diabetes_data.csv came from.

What this notebook covers
Initial inspection — checking column types, non-null counts, and summary statistics with .info() and .describe()
Simulated missing values — the source data has no nulls, so a few values in age and sudden_weight_loss are deliberately set to NaN to practice imputation
Categorical encoding — converting gender (Male/Female) to a numeric binary feature
Missing value imputation — filling gaps using column mean
Distribution visualization — histograms across all features to check for skew and class balance
Final validation — confirming zero remaining missing values
Tools used
pandas — data loading, cleaning, and transformation
numpy — numeric operations
matplotlib — visualization
How to run
bash
pip install -r requirements.txt
jupyter notebook diabetes_preprocessing.ipynb

Place diabetes_data.csv in the same directory (or update the file path in the notebook) before running.

Key takeaways
Mean imputation is a reasonable baseline for small, randomly-missing gaps, but isn't always the right choice for real-world missing data — worth revisiting with median or model-based imputation depending on the missingness pattern
gender was the only feature requiring categorical encoding; all symptom columns were already binary
Next steps for this dataset: feature scaling, train/test split, and a baseline classification model (e.g. logistic regression)
Project status

This is a learning project focused specifically on the data preprocessing stage. Modeling and evaluation are not yet included.
