
## 🚀 Week 2: Building ML Models

| Metric / Parameter | Details |
| :--- | :--- |
| **Baseline ("Always Stay")** | Accuracy: `0.73` |
| **Best Performing Model** | Random Forest |
| **Model Metrics** | AUC: `0.84` \| Recall: `0.78` @ threshold `0.35` |
| **Top Churn Drivers** *(Permutation Importance)* | Contract type, Monthly charges, Tenure |
| **Decision Threshold** | `0.35` (Chosen to minimize false negatives and catch at-risk customers early, balancing retention costs against revenue loss) |
| **Engineered Features** | `Tenure_to_Charges_Ratio`, `Total_Services_Used` |
| **Feature Engineering Impact** | AUC: `0.79` \(\rightarrow\) `0.84` |
| **Biggest Takeaway** | Strategic feature engineering and careful threshold tuning drastically improve model sensitivity on imbalanced customer churn datasets. |

## 🚀 Week 3: Model Optimization and Unsupervised Learning

### Overview & Methodology
This module covers advanced machine learning techniques, hyperparameter optimization, model evaluation under cross-validation, and unsupervised learning workflows (K-Means clustering and Principal Component Analysis) applied to customer churn prediction.

### Key Results & Metrics
- **Split-to-Split Stability**: Split-to-split accuracy range across 20 random seeds: 0.792 to 0.824
- **5-Fold Cross-Validation AUC**: 
  - Logistic Regression: $0.842 \pm 0.0114$
  - Random Forest: $0.851 \pm 0.0121$
  - XGBoost: $0.859 \pm 0.0108$
- **Hyperparameter Optimization (Random Forest)**: 
  - Best parameters: `{'n_estimators': 200, 'max_depth': 10, 'min_samples_split': 5}`
  - Tuning execution time comparison: Grid Search (45s) vs. Randomized Search (12s)
- **Final Model Evaluation**: 
  - Test AUC of final optimized model (evaluated once): **0.862**

### Unsupervised Learning & Dimensionality Reduction
- **Customer Segments ($k = 3$)**:
  - *High-Risk Month-to-Month*: 48% churn rate, short tenure, fiber optic internet preference.
  - *Loyal Long-Term*: 7% churn rate, multi-year contracts, stable payment methods.
  - *Moderate-Risk Fiber Users*: 26% churn rate, intermediate tenure with high monthly charges.
- **Principal Component Analysis (PCA)**: 
  - 14 of 30 components explain 90% of the cumulative variance.

### Key Takeaway
- **Biggest Lesson**: Proper pipeline encapsulation of preprocessing steps (such as scaling and imputation) prevents data leakage during cross-validation and guarantees robust, unbiased generalization on unseen data.
