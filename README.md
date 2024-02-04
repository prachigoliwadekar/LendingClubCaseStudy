# Lending Club Case Study

## Table of Contents
* [Problem Statement](#problem-statement)
* [Objectives](#objectives)
* [Data Understanding](#data-understanding)
* [Data cleaning and manipulation](#data-cleaning-and-manipulation)
* [Data Analysis](#data-analysis)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)
* [Glossary](#glossary)
* [Team](#team)

## Problem Statement

Lending Club is the largest online loan marketplace, facilitating personal loans, business loans, and financing of medical procedures. Borrowers can easily access lower interest rate loans through a fast online interface. 

Like most other lending companies, *lending loans to ‘risky’* applicants is the largest source of financial loss *(called credit loss)*. The **credit loss** is the amount of money lost by the lender when the borrower refuses to pay or runs away with the money owed.

In other words, **borrowers** who **default** cause the largest amount of **loss to the lenders**. In this case, the customers labeled as *'charged-off' are the 'defaulters'*.

Help the organization identify such borrowers and stay away from them.

## Objectives

The exercise here is to identify the **defaulters**. Identify the parameters that can help us to find the potential candidates who could **default**. 
This will help the organization to reduce lending loans to such risky applicants. This will also help in reducing the **credit loss** of the company.

Using EDA on the data set provided("loan_1.csv"), we can identify the parameters that infer to risky loan applicants.

In other words, **the company wants to understand the driving factors (or driver variables)** behind loan default, i.e. the variables that are strong indicators of default.  The company can utilize this knowledge for its portfolio and risk assessment. 

## Data Understanding

The data provided has loans that are accepted and fall in 3 categories - 
-Fully paid: Applicant has fully paid the loan (the principal and the interest rate)
-Current: Applicant is in the process of paying the installments, i.e. the tenure of the loan is not yet completed. These candidates are not labeled as 'defaulted'.
-Charged-off: Applicant has not paid the installments in due time for a long period of time, i.e. he/she has defaulted on the loan 

Few of the important columns of this dataset are - 
- loan_amt
- funded_amnt
- funded_amnt_inv
- int_rate
- installment
- annual_inc
- dti
- home_ownership
- term
- grade


## Data cleaning and manipulation

Data cleaning on columns - 
- Find and remove all columns with all NULL values
- Find and remove all columns with unique values
- Correct the data type and standardise columns like - funded_amnt, loan_amt, funded_amnt_inv
- Cleaning of the columns to make them more informative -  int_rate, term
- Add derived columns like issue_d - derived to issue_month, issue_year
- Formation of bucket column based on data range - issue_q, dti_b, loan_amnt_b, annual_inc_b, int_rate_b, funded_amt_b, funded_amt_inv_b

Data cleaning on rows -
- Considered rows with loan_status != "Current"
- Remove outliner rows for annual_inc and loan_amt
- Drop rows with empty values in emp_length and pub_rec_bankruptcies

## Data Analysis

- Univariate Analysis
    -- loan_amt
    -- funded_amnt
    -- funded_amnt_inv
    -- int_rate
    -- installment
    -- annual_inc
    -- dti

- Unordered Categorical Variable Analysis
    -- home_ownership
    -- purpose
    -- addr_state

- Ordered Categorical Variable Analysis
    -- term
    -- grade
    -- emp_length
    -- pub_rec_bankruptcies

- Derived Variable Analysis
    -- issue_year
    -- issue_month
    -- issue_q
    -- loan_amnt_b

- Heat Map - funded_amnt', 'funded_amnt_inv', 'loan_amnt'
- Bar charts - annual_inc_b, dti_b

- Bivariate Analysis
    -- term v/s loan_status
    -- grade v/s loan_status
    -- emp_length v/s loan_status
    -- home_ownership v/s loan_status
    -- purpose v/s loan_status
    -- addr_state v/s loan_status
    -- pub_rec_bankruptcies v/s loan_status
    -- issue_q v/s loan_status
    -- annual_inc_b v/s loan_status
    -- loan_amnt_b v/s loan_status
    -- int_rate_b v/s loan_status

- Correlation Analysis
      -- "int_rate","term","dti","pub_rec_bankruptcies","emp_length","installment","loan_amnt","annual_inc","issue_year","id","issue_month"
      -- "int_rate","term","dti","pub_rec_bankruptcies","emp_length","loan_amnt","annual_inc"
      -- 'term', 'int_rate', 'dti'
  
- Pair Plot - 'loan_amnt', 'annual_inc', 'int_rate', 'dti'

## Conclusions


## Technologies Used
- [Python - Version 3.12.1](https://www.python.org/downloads/release/python-3121/)
- [numpy - Version 1.26.2](https://github.com/numpy)
- [pandas - Version 2.1.4](https://github.com/pandas-dev/pandas)
- [matplotlib - Version 3.8.2](https://github.com/matplotlib)
- [seaborn - Version 0.13.1](https://github.com/seaborn)
- [Jupyter Notebook - Version 7.0.6]()
- [JupyterLab - Version 4.0.9]()

## Glossary
- EDA - Exploratory Data Analytics

## Team
* [Prachi Goliwadekar]
* [Rathnagiri Nagarajan]
