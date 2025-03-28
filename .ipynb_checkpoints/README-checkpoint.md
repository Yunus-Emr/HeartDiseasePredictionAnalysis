# ❤️ Heart Disease Prediction with Machine Learning

This project aims to predict the risk of heart disease based on various health-related features using machine learning techniques. The motivation behind this study is to contribute to early diagnosis and preventive healthcare by leveraging data science.

## 📁 Project Structure

HeartDiseaseProject/ │ ├── data/ │ ├── raw/ # Original dataset │ └── processed/ # Cleaned and transformed dataset │ ├── notebooks/ │ ├── 01_EDA.ipynb # Exploratory Data Analysis │ ├── 02_FeatureEng.ipynb# Feature Engineering │ └── 03_Modeling.ipynb # Modeling and Evaluation │ ├── models/ # Trained model files (.pkl) ├── outputs/ │ ├── figures/ # Visualizations │ └── reports/ # Project reports and summaries │ ├── requirements.txt # Python libraries used └── README.md # Project overview (this file)


## 🧠 Machine Learning Models

We implemented and evaluated the following models:

- **Naive Bayes**
- **Support Vector Classifier (SVC)**
- **XGBoost Classifier**

### Evaluation Metrics

We used:
- Accuracy
- Precision, Recall, F1-Score
- Cross-Validation Score
- Confusion Matrix
- ROC-AUC Curve

### Result Summary

| Model        | Accuracy | ROC-AUC |
|--------------|----------|---------|
| Naive Bayes  | 0.81     | 0.50    |
| SVC          | 0.54     | 0.49    |
| XGBoost      | 0.78     | 0.50    |

Despite relatively high accuracy in some models, the **ROC-AUC scores indicate low discriminative power** due to class imbalance and dataset limitations.

## Highlights

- Performed detailed Exploratory Data Analysis (EDA)
- Handled missing values using KNN imputation
- Applied feature encoding and scaling
- Trained multiple models and compared results
- Tried class imbalance techniques like `scale_pos_weight` and `SMOTE`

## Installation

```bash
pip install -r requirements.txt

📊 Dataset

The dataset contains 2000 samples and 20+ features including:

    Demographics (Age, Gender)

    Lifestyle (Exercise, Smoking, Sleep)

    Medical (Blood Pressure, Cholesterol, BMI, CRP, Diabetes)

    Target: Heart Disease Status (Yes / No)

Conclusion

This project demonstrates a full end-to-end machine learning workflow including preprocessing, model comparison, and evaluation. The ROC-AUC results suggest that the current dataset may not be ideal for robust prediction. Future work may involve using a more balanced dataset or applying advanced techniques such as deep learning or feature synthesis.
Author & Contact

Created by [Yunus Emre Akca]
📧 yunusemreakc58@@gmail.com
🔗 www.linkedin.com/in/yunus-emre-akca-900a61268