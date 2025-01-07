# Optimizing Loan Decisions with Machine Learning

## Project Overview
LoanTap is a digital platform offering tailored financial solutions to millennials. This project focuses on developing a machine learning model to evaluate the creditworthiness of individuals applying for personal loans. The objective is to assess whether a credit line should be extended to an applicant and provide business recommendations on repayment terms.

---

## Problem Statement
Given a set of attributes for an individual, determine:
1. Should a credit line be extended?
2. If yes, what should the repayment terms be?

---

## Data Description
The dataset contains attributes related to borrowers and their financial history. Key features include:
- **Loan amount** (`loan_amnt`): Amount of loan applied for.
- **Interest rate** (`int_rate`): Interest rate on the loan.
- **Employment details** (`emp_length`, `emp_title`): Employment duration and job title.
- **Credit history** (`dti`, `revol_util`, `earliest_cr_line`): Debt-to-income ratio, revolving line utilization, and earliest credit line.
- **Loan status** (`loan_status`): Target variable indicating loan repayment status.

For a complete list of features, refer to the code comments.

---

## Project Workflow
1. **Data Cleaning and Preprocessing**:
   - Handled missing values using imputation strategies (mean imputation, grouping).
   - Dropped redundant and highly correlated features (e.g., `installment`).
   - Applied transformations to normalize and encode categorical variables.
2. **Exploratory Data Analysis (EDA)**:
   - Visualized relationships between features and loan status using boxplots, countplots, and heatmaps.
   - Detected and treated outliers using interquartile range (IQR) and Z-scores.
3. **Feature Engineering**:
   - Encoded categorical variables using label and one-hot encoding.
   - Scaled numerical features for model compatibility.
4. **Model Building**:
   - Implemented logistic regression as the primary classification model.
   - Applied SMOTE to handle class imbalance in the dataset.
   - Split data into training, validation, and test sets.
5. **Model Evaluation**:
   - Evaluated using accuracy, precision, recall, F1-score, and ROC-AUC metrics.
   - Optimized hyperparameters for improved performance.

---

## Results
- **Training Accuracy**: Achieved an accuracy of ~90.66% on the training set.
- **Validation Accuracy**: Achieved an accuracy of ~90.73% on the validation set.
- False positive cases are more risky for this industry, hence we focus on the precision metric.
- **Model Performance Metrics**:
  - Precision: 0.96
  - Recall: 0.85
  - F1-Score: 0.90
  - ROC-AUC: 0.96

---

## Business Recommendations and Actionable Insights
1. **Credit Extension Criteria**:
   - Approve loans for individuals with stable employment, low debt-to-income ratios, and minimal derogatory records.
   - Consider higher creditworthiness scores for borrowers with long-standing credit histories.
2. **Risk Mitigation**:
   - Implement higher interest rates or collateral requirements for high-risk applicants.
   - Encourage borrowers to consolidate debt to reduce overall risk.
3. **Future Improvements**:
   - Integrate additional features such as social credit scores or utility bill payment histories to enhance prediction accuracy.
   - Explore advanced algorithms like Random Forest or XGBoost for better performance.


## Future Scope
- Enhance the model by incorporating feature selection techniques to avoid overfitting.
- Deploy the model using Flask or FastAPI for real-time loan application evaluation.
- Create a user-friendly dashboard to visualize applicant data and loan decisions.

## Prerequisites
1. Python 3.8 or higher.
2. Jupyter Notebook or any Python IDE (e.g., VS Code, PyCharm).
3. Libraries specified in `requirements.txt` (e.g., pandas, numpy, scikit-learn, matplotlib, seaborn, imbalanced-learn).
