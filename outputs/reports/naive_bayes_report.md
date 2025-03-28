#### Comments and Conclusion 

##### 1. Model Overview
- **Model Type:** Gaussian Naive Bayes  
- **Assumption:** Features are conditionally independent.  
- **Rationale:** This model was chosen because there is little to no correlation between features, making it a suitable candidate.

---

##### 2. Performance Metrics
- **Accuracy:** 0.8065  
- **Cross-Validation Score (10-Fold):** 0.806  
- **Precision (No / Yes):** 0.81 / 0.00  
- **Recall (No / Yes):** 1.00 / 0.00  
- **F1-Score (No / Yes):** 0.89 / 0.00  
- **Support (No / Yes):** 1613 / 387  

**Interpretation:**  
The model performs well on the dominant class ("No") but fails completely to predict the minority class ("Yes"). This is a clear indication of class imbalance affecting the classifier's performance.

---

##### 3. ROC Curve & Confusion Matrix
- **ROC AUC Score:** 0.50  
- **ROC Curve:** Indicates random guessing  
- **Confusion Matrix:**

**Interpretation:**  
The ROC AUC score of 0.50 suggests the model does not distinguish between classes at all. The confusion matrix confirms the model only predicts "No" for all instances.

---

##### 4. Conclusion & Recommendations
- **Strength:** High accuracy and strong performance on the majority class.
- **Weakness:** Completely fails to classify the minority class ("Yes").
- **Cause:** Severe class imbalance (No: ~80%, Yes: ~20%).

**Next Steps:**
- Apply **SMOTE** to balance the dataset.
- Experiment with **class_weight='balanced'** in other models.
- Try more powerful classifiers like **SVC** and **XGBoost**.

