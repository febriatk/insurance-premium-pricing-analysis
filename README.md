# INSURANCE PREMIUM PRICING ANALYSIS

This project aims to analyze factors affecting health insurance charges and develop a simple customer risk segmentation model using Python. The analysis focuses on identifying important variables related to insurance pricing, such as age, BMI, and smoking status.

In addition, this project implements a risk scoring system to classify customers into different risk levels that can support insurance premium pricing evaluation.

## Objective
- Perform data cleaning and exploratory data analysis (EDA)
- Identify variable affecting insurance charges
- Analyze relationships between customer characteristics and insurance costs
- Develop customer risk scoring and risk level segmentation
- Generate business insights related to insurance premium pricing

## Dataset
Source: Kaggle 
[Medical Insurance Cost Dataset](https://www.kaggle.com/datasets/mosapabdelghany/medical-insurance-cost-dataset)

Features:
- age: age of primary beneficiary
- sex: gender of beneficiary (male, female)
- bmi: Body Mass Index, a measure of body fat based on height and weight
- children: number of children covered by health insurance
- smoker: smoking status of the beneficiary (yes, no)
- region: residential region in the US (northeast, northwest, southeast, southwest)
- charges: medical insurance cost billed to the beneficiary

## Tools
Python with libraries Pandas, Matplotlib, Seaborn

## Project Workflow
### 1. Data Understanding
Inital exploration was performed to understand:
- dataset structure
- data types
- number of rows and columns
<img width="807" height="460" alt="{55CF2A13-D05D-4587-956F-1C4F756F13DB}" src="https://github.com/user-attachments/assets/24d45b62-faec-4f50-bb26-ed9182c4eecf" />

Output:
- Total data: 1338 rows
- Dataset contains numerical and categorical variables

### 2. Data Cleaning
- Missing Value Check
<img width="809" height="346" alt="{2C1C43CB-236E-4541-BDBB-1675932E8DFE}" src="https://github.com/user-attachments/assets/3079f6d7-4db8-49fa-bb18-c93ba70d7982" />

No missing values were found in the dataset
- Duplicate Check
<img width="811" height="385" alt="{7E3EE343-5B68-46FD-AEE1-58EF346D5C75}" src="https://github.com/user-attachments/assets/e2fe0d21-5cc0-4344-986d-a856ae0508d7" />

1 duplicate row found and succesfully removed
- Outlier Analysis
  Boxplot analysis was performed on insurance charges
  <img width="810" height="547" alt="{F1943446-AD18-40B9-984D-2406BC8C22A0}" src="https://github.com/user-attachments/assets/66b6edfb-360c-4d02-ba32-06afb7447f05" />

  Several extreme values were identified in the charges variable, indicating the presence of customers with significantly higher medical cost compared to the majority of customers and potentially represent high risk insurance customers.

