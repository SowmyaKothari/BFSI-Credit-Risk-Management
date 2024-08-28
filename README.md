# BFSI-Credit-Risk-Management
# Loss Given Default (LGD) Prediction Model

## Project Overview

In the banking industry, managing credit risk is a critical aspect of operations, especially in the context of regulatory frameworks like Basel norms. A key component of credit risk management is the computation of Expected Credit Loss (ECL), which comprises the Probability of Default (PD), Loss Given Default (LGD), and Exposure at Default (EAD). This project focuses on developing a model to estimate the Loss Given Default (LGD) for defaulted loan accounts.

As a business analyst working for a bank, the objective of this project is to build a statistical model that can predict the LGD for borrowers. The LGD represents the proportion of the total loan amount that the bank expects to lose if a borrower defaults. A more accurate prediction of LGD helps the bank in better credit risk management and provisioning, ensuring compliance with regulatory standards and improving decision-making processes.

## Problem Statement

The task is to estimate the LGD for defaulted accounts using provided datasets that include information on defaulted loan accounts, collateral values, and the amounts recovered through various collection methods. The LGD is a crucial metric for calculating the ECL and is used in conjunction with the PD to provide a comprehensive view of potential losses from loans.

### Business Objective

- Develop a model to predict the Loss Given Default (LGD) for defaulted loan accounts.
- Use the LGD predictions to enhance the bank’s ability to manage credit risk, comply with regulatory standards, and make informed decisions about loan provisioning and high-risk loans.

## Dataset Description

The project utilizes three datasets, which together provide a comprehensive view of the loan accounts, repayment history, and customer financial behavior. These datasets are:

1. **main_loan_base.csv**: Contains information about 20,000 loan accounts, including loan amount, collateral value, loan type, customer details, and loan performance metrics like missed repayments and cheque bounces.

2. **repayment_base.csv**: Details the repayments made on the loan accounts, including the repayment date and amount. This dataset is crucial for understanding the recovery process and calculating the LGD.

3. **monthly_balance_base.csv**: Provides monthly bank balance details of the customers throughout the loan tenure, offering insights into their financial stability and repayment capacity.

The datasets can be merged using the `loan_acc_num` as a common key, allowing for a comprehensive analysis of each loan account.

## Approach

The approach to building the LGD prediction model involves several steps:

1. **Understanding the Business Problem**: Gain a deep understanding of the business context and the role of LGD in credit risk management and ECL computation.

2. **Data Exploration and Understanding**: Thoroughly explore the datasets, understanding the variables, data types, and distributions. Special attention is given to the target variable (LGD), which needs to be calculated using provided formulas.

3. **Data Preparation**: 
   - Merge the datasets using `loan_acc_num` as the common key.
   - Handle missing values, outliers, and data type mismatches to ensure data integrity.
   - Perform feature engineering to create new variables that could enhance model performance.

4. **LGD Calculation**: 
   - Calculate the LGD using the formula: 
   \[
   \text{LGD} = \frac{\text{Loan Amount} - \text{Recovered Amount}}{\text{Loan Amount}}
   \]
   where the Recovered Amount is derived from collateral values and repayments.

5. **Model Development**: 
   - Use statistical or machine learning techniques to develop the LGD prediction model.
   - Evaluate the model's performance using appropriate metrics and ensure it generalizes well to unseen data.

6. **Model Implications**: 
   - Discuss the implications of the model for the bank’s business operations, focusing on risk management and regulatory compliance.
   - Identify key success areas and potential improvements for future iterations of the model.

## Business Impact

The model developed in this project will assist the bank in more accurately predicting potential losses from defaulted loans. By integrating the LGD predictions with the PD model, the bank can better manage its credit risk, make informed decisions about loan provisioning, and enhance compliance with regulatory standards such as Basel norms.

---

This project demonstrates the application of data science techniques in financial risk management, specifically in estimating the Loss Given Default (LGD) for a bank’s loan portfolio. The project highlights the importance of predictive modeling in improving risk management practices and ensuring regulatory compliance.
