
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
