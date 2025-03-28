#### Comments and Conclusion X

* Despite being one of the most powerful ensemble methods, XGBoost did not perform as expected in our dataset. Although it showed decent accuracy (77.95%) and cross-validation score (78.45%), the ROC AUC score (0.50) clearly indicated that the model fails to differentiate between classes better than random chance.

* Even after using class balancing techniques such as scale_pos_weight and SMOTE oversampling, the improvement in recall and ROC-AUC was marginal at best. The results suggest that the underlying structure of the data does not favor non-linear boosting-based classifiers or may lack strong informative features for classification.

* Thus, although XGBoost is theoretically a strong model, in this context, it struggled due to class imbalance and possibly insufficient feature signal strength

