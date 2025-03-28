#### Comments and Conclusion 

* Although the SVC model provided improved F1-Score and Recall metrics compared to Naive Bayes, the overall model performance is still unsatisfactory. The ROC-AUC score remains close to **0.50**, indicating that the model is no better than random guessing in distinguishing between the positive and negative classes.

* Different kernel functions including `poly` and `sigmoid` were also tested, but they similarly resulted in ROC-AUC scores around **0.50**. This suggests that the SVC model may not be the most suitable choice for this dataset.

* Despite tuning for class imbalance and enabling probabilistic predictions, SVC failed to achieve a reliable performance. Therefore, we will proceed with trying more powerful models like **XGBoost**, which are often better suited for structured tabular data with complex feature interactions.