🧠 Azure Machine Learning Studio with UCI Datasets


📋 **Project Overview**

This project demonstrates an end-to-end **no-code machine learning pipeline** built using **Azure Machine Learning Designer**. The goal is to predict customer churn using the Churn Modeling Dataset, identifying which customers are likely to leave the bank.

Built as part of my final year practical assessment, this project showcases how Azure ML makes machine learning accessible without writing a single line of code!


🎯 **Business Problem**
> *"Can we predict which customers are likely to churn (leave the bank) based on their demographic and account information?"*

 📊 **Dataset Overview**
- **Source:** Churn Modeling Dataset (Bank Customers)
- **Rows:** 10,000 customer records
- **Target:** `Exited` (0 = Stayed, 1 = Churned)
- **Features:** Gender, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary


🚀 **Project Features**

| Feature                            | Description                                                     |
|------------------------------------|-----------------------------------------------------------------|
| ✅ **No-Code Pipeline**           | Built entirely using Azure ML Designer drag-and-drop             |
| ✅ **Data Preprocessing**         | Cleaning missing values, feature selection, categorical encoding |
| ✅ **Binary Classification**      | Predicts churn (Yes/No) using Two-Class Boosted Decision Tree    |
| ✅ **Model Evaluation**           | Accuracy, Precision, Recall, F1-Score metrics                    |
| ✅ **Reproducible**               | Complete pipeline can be cloned and re-run                       |
| ✅ **Article & Walkthrough**      | Detailed Medium article with screenshots and explanations        |



🛠️ **Technologies Used**

| Category               | Technologies                                    |
|------------------------|-------------------------------------------------|
| **Cloud Platform**     | Microsoft Azure                                 |
| **ML Service**         | Azure Machine Learning Studio                   |
| **Pipeline Tool**      | Azure ML Designer (Classic Prebuilt Components) |
| **Compute**            | Azure ML Compute Cluster                        |
| **Data Storage**       | Azure Blob Storage                              |
| **ML Algorithm**       | Two-Class Boosted Decision Tree                 |
| **Metrics**            | Accuracy, Precision, Recall, F1-Score           |


Model Performance**

After training the model using **Two-Class Boosted Decision Tree**, here are the evaluation metrics:

| Metric          | Score | Interpretation                         |
|-----------------|-------|----------------------------------------|
| **Accuracy**    | ~85%  | Model correctly predicts 85% of cases  |
| **Precision**   | ~75%  | When predicting churn, 75% are correct |
| **Recall**      | ~55%  | Model catches 55% of actual churners   |
| **F1-Score**    | ~65%  | Balance between Precision and Recall   |

### 📉 **Confusion Matrix (Expected)**

Predicted
Stayed Churned
Actual Stayed [ 85% 15% ]
Churned [ 45% 55% ]

![image](https://github.com/user/repo/assets/<img width="996" height="707" alt="Picture81" src="https://github.com/user-attachments/assets/323a080b-6a50-4ed8-a78c-e1ce44f01e79" />
xxxx)

![image](https://github.com/user/repo/assets/xxxx)<img width="677" height="431" alt="Picture82" src="https://github.com/user-attachments/assets/1ccfebaa-f503-4c38-8510-3de4aa842378" />

![image](https://github.com/user/repo/assets/xxxx)<img width="760" height="421" alt="Picture83" src="https://github.com/user-attachments/assets/55a50a77-dbc1-4099-92c0-95be24231e35" />

![image](https://github.com/user/repo/assets/xxxx)<img width="787" height="425" alt="Picture84" src="https://github.com/user-attachments/assets/99b9159b-1f1e-40a3-8b18-dd4f34bb82f7" />



## 📝 **Key Learnings & Challenges**

### ✅ **What Worked Well**
- Azure ML Designer's drag-and-drop interface made pipeline building intuitive
- Built-in preprocessing components saved significant development time
- Automatic compute management simplified model training

### ⚠️ **Challenges Overcome**
1. **Data Integrity**: Initially included `Exited` in Clean Missing Data → Had to remove it to preserve target column
2. **Categorical Data**: `Gender` (Male/Female) required conversion to numerical using `Convert to Indicator Values`
3. **Feature Selection**: Excluded irrelevant columns (`RowNumber`, `CustomerId`, `Surname`) to reduce noise

### 💡 **Improvement Suggestions**
- **Hyperparameter Tuning**: Use `Tune Model Hyperparameters` for better performance
- **Feature Engineering**: Create new features (e.g., Age Group, Balance Category)
- **SMOTE**: Handle class imbalance (more stayed than churned)
- **Cross-Validation**: Use k-fold validation for more reliable metrics

---

## 🚀 **How to Replicate This Project**

### Prerequisites
- Azure Subscription (Free Tier works)
- Azure ML Workspace
- Basic understanding of ML concepts

### Steps

1. **Create Azure ML Workspace**
   - Go to Azure Portal → Machine Learning → Create New Workspace

2. **Upload Dataset**
   - Download Churn Modeling Dataset from Kaggle
   - Go to Data → Create → From Local Files

3. **Build Pipeline**
   - Open Designer → Create new pipeline
   - Drag components in this order:

    Dataset → Clean Missing Data → Select Columns →
    Convert to Indicator Values → Split Data →
    Two-Class Boosted Decision Tree → Train Model →
    Score Model → Evaluate Model


   4. **Configure Components**
- **Clean Missing Data**: Select numerical columns only
- **Select Columns**: Choose relevant features (exclude target)
- **Convert to Indicator Values**: Select `Gender`
- **Split Data**: 0.7 fraction
- **Train Model**: Set Label = `Exited`

5. **Submit Pipeline**
- Configure compute cluster
- Click Submit
- Wait for completion (~5-10 minutes)

6. **View Results**
- Go to Jobs → Click experiment → Right-click Evaluate Model → View Results

---
Screenshots

![image](https://github.com/user/repo/assets/xxxx)<img width="1046" height="752" alt="Picture78" src="https://github.com/user-attachments/assets/8071f27f-d8f5-4d18-b825-6ebb0f07e8d8" />


![image](https://github.com/user/repo/assets/xxxx)<img width="506" height="565" alt="Picture80" src="https://github.com/user-attachments/assets/c35fcd61-0ca8-4077-ab89-254b86cd6e08" />



📚 **Resources & References**

- [Azure Machine Learning Documentation](https://learn.microsoft.com/en-us/azure/machine-learning/)
- [Azure ML Designer Documentation](https://learn.microsoft.com/en-us/azure/machine-learning/concept-designer)
- [Churn Modeling Dataset (Kaggle)](https://www.kaggle.com/datasets/)
- [Medium Article - Full Walkthrough](https://medium.com/@udsewmini99/practical-for-cloud-application-development-a7534f827f94)
 

