Credit Card Default Dataset
1. Dataset Description
The Credit Card Default dataset contains information about credit card
clients, including demographic details, credit limits, repayment status,
bill amounts and previous payment amounts. It also records whether a
client defaulted on their payment in the following month.
2. Dataset Information
- File name: default of credit card clients.xls
- Number of records: 30,000
- Number of features: 23 input features
- Target variable: default payment next month
- Total columns: 25 (including the ID column)
- File format: Excel (.xls)
- Missing values: No missing values were found in the inspected
  data rows after identifying the first row as the column headings.
3. Objective
The main objective of this dataset is to analyse customer credit
information and identify patterns associated with credit card payment
defaults. It can be used to develop machine learning models that predict
whether a client is likely to default on the next month's payment.
4. Features Description
  Feature                             Description
  ID                                Identification number of each
client

  LIMIT_BAL                         Amount of given credit (in NT
dollars)

  SEX                               Gender category

  EDUCATION                         Education category

  MARRIAGE                          Marital status category

  AGE                               Age of the client

  PAY_0                             Repayment status in September 2005

  PAY_2                             Repayment status in August 2005

  PAY_3                             Repayment status in July 2005

  PAY_4                             Repayment status in June 2005

  PAY_5                             Repayment status in May 2005

  PAY_6                             Repayment status in April 2005

  BILL_AMT1                         Bill statement amount for September
2005

  BILL_AMT2                         Bill statement amount for August
2005

  BILL_AMT3                         Bill statement amount for July 2005

  BILL_AMT4                         Bill statement amount for June 2005

  BILL_AMT5                         Bill statement amount for May 2005

  BILL_AMT6                         Bill statement amount for April
2005

  PAY_AMT1                          Payment amount in September 2005

  PAY_AMT2                          Payment amount in August 2005

  PAY_AMT3                          Payment amount in July 2005

  PAY_AMT4                          Payment amount in June 2005

  PAY_AMT5                          Payment amount in May 2005

  PAY_AMT6                          Payment amount in April 2005
default payment next month        Indicates whether the client
defaulted next month (target
variable)
5. Target Variable
The target variable is default payment next month. - 0 -- No
default - 1 -- Default

In the inspected dataset, 23,364 records have a target value of 0 and
6,636 records have a target value of 1.
6. Dataset Structure
The dataset contains 30,000 client records and 25 columns, including the
client ID, 23 explanatory features and the target variable. Each row
represents one credit card client.
7. Possible Applications
- Exploratory Data Analysis (EDA)
- Customer credit behaviour analysis
- Default risk analysis
- Data visualisation
- Classification using machine learning
- Credit card default prediction
8. Data Preprocessing
The first row in the supplied Excel file contains the actual column
names. When loading the file, use the first row as the header and remove
the ID column from the model features if it is not useful for
prediction.

Example:
import pandas as pd

df = pd.read_excel("default of credit card clients.xls", header=1)

# Separate the target variable
X = df.drop(columns=["ID", "default payment next month"])
y = df["default payment next month"]
Check category codes, data types, class distribution and feature
relationships before modelling. The PAY_0 name is retained as it
appears in the dataset.
9. Conclusion
The Credit Card Default dataset is useful for analysing customer
repayment behaviour and studying factors related to credit risk. It
provides a practical dataset for classification and predictive
modelling.
