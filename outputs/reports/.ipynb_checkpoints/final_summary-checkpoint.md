## Final Evaluation and Project Summary

### Project Objective
The aim of this project was to predict the likelihood of heart disease in individuals based on various health, lifestyle, and biological features. Through this analysis, we sought to explore the relationships between these features and heart disease, and evaluate how well different machine learning models can perform on a real-world imbalanced dataset.

---

### What We Did

1. **Initial Data Overview**
   - Explored variable distributions
   - Assessed target imbalance (80% No, 20% Yes)

2. **Missing Value Handling & Outlier Detection**
   - Applied KNN Imputer for numeric missing values
   - Dropped ‘Alcohol Consumption’ due to 25% missingness
   - No significant outliers found

3. **EDA (Exploratory Data Analysis)**
   - Examined feature relationships with heart disease
   - Used statistical tests and visualizations (Chi-square, t-test, boxplot, mosaic, violin, etc.)
   - Found very few features with strong explanatory power

4. **Feature Engineering**
   - Performed encoding, scaling (Z-score), KNN imputation
   - Checked multicollinearity and feature correlations
   - No significant multicollinearity observed

5. **Modeling**
   - Applied **Naive Bayes**, **SVC**, and **XGBoost**
   - Addressed class imbalance using techniques such as `class_weight`, `scale_pos_weight`, and **SMOTE**
   - Evaluated using metrics: **Accuracy**, **F1-Score**, **Recall**, **ROC-AUC**, and **Confusion Matrix**

---

### Key Results

| Model        | Accuracy | F1-Score (Yes) | ROC AUC | Notes                          |
|--------------|----------|----------------|---------|--------------------------------|
| Naive Bayes  | 80.65%   | 0.00           | 0.50    | Predicts only majority class   |
| SVC (RBF)    | 54.20%   | 0.25           | 0.49    | Slight recall improvement      |
| XGBoost      | 77.95%   | 0.06           | 0.50    | SMOTE + class weight had little effect |

---

### Final Conclusion

- Despite extensive preprocessing and the use of various class imbalance handling techniques, **no model achieved meaningful class separation**.
- Most features showed **weak or no statistical relationship** with the target variable.
- This highlights the critical importance of **feature quality**, and that **not all datasets are model-friendly**.
- Nevertheless, the project demonstrates a robust data science workflow, with effective **EDA**, **feature engineering**, and **model evaluation**.
