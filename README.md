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

### 3. Exploratory Data Analysis (EDA)
- Distribution of Age
  <img width="811" height="773" alt="{9E5FF20E-E789-4B87-AE5B-D9308CAFD527}" src="https://github.com/user-attachments/assets/98305904-3f43-4b93-8522-b46a4ee0cc62" />

  Customer ages are relatively well distributed across age ranges, with a slightly higher concentration in younger age groups.
- Distribution of BMI
  <img width="811" height="772" alt="{B28D3289-ADED-4D29-8260-60463BB2C429}" src="https://github.com/user-attachments/assets/0fdb2ba7-86e1-4090-aa0d-5cd8c9ed2e10" />

  Most customers fall into the overweight and obese BMI categories, indicating potential health risks that may influence insurance charges.
- Distribution of Insurance Charges
  <img width="807" height="773" alt="{C17FFFDD-FCF1-4673-84DF-4FD544293207}" src="https://github.com/user-attachments/assets/df91bece-5298-4e3b-bae2-d3d907099154" />

  The distribution of insurane charges is highly right skewed, where most customers generate low to medium charges while a smaller number of customers generate extremely high insurance costs.

### 4. Correlation Analysis
A correlation heatmap was created to identify relationship between variables and insurance charges.
<img width="815" height="549" alt="{97B2A33A-286F-4CDB-9D69-D18D26D76815}" src="https://github.com/user-attachments/assets/1b02ef15-9f46-4e9e-8331-52355c282395" />

Smoking status shows the strongest positive relationship with insurance charges compared to other variables. This indicates that smokers tend to generate significantly highly medical insurance costs.

### 5. Feature Engineering
- Age Category
  Customer age was categorized based on Kemenkes standards
  <img width="809" height="561" alt="{351089BD-F865-4DD2-A6C8-2D1280B16612}" src="https://github.com/user-attachments/assets/db25570f-ca58-4620-8775-a1b26411177c" />

- BMI Category
  BMI categories were created based on WHO standards
  <img width="813" height="490" alt="{BC15B224-91F8-4E73-A86E-69D69625F618}" src="https://github.com/user-attachments/assets/e2021563-19c1-41db-8b9f-45ac3928f1ec" />

### 6. Risk Scoring
A simple risk scoring system was developed using age, BMI category, and smoking status
- Age Score
  <img width="808" height="196" alt="{B455EC4A-7E10-4AF0-837A-CCD2A82D9086}" src="https://github.com/user-attachments/assets/ce472fd3-230f-4afc-8ae0-f1ca3abcf7ee" />

- BMI Score
  <img width="808" height="191" alt="{3A0CECF8-10C9-4953-8609-C8415A6555A3}" src="https://github.com/user-attachments/assets/21e3a739-7f3e-47f4-b3db-320d9a55f8cf" />

- Smoker Score
  <img width="810" height="153" alt="{7BF4DD75-361B-4B56-A14D-1ECBFEC8EF56}" src="https://github.com/user-attachments/assets/2d58a74a-ad68-419f-8138-5c89ff326b46" />

  Smoking status received the highest score because it showed the strongest correlation with insurance charges.

- Total Risk Score
  The total risk score was calculated by summing age score, BMI score, and smoker score
  <img width="811" height="454" alt="{44CFE5FD-1B05-4C3C-827D-502482FFA658}" src="https://github.com/user-attachments/assets/f7632b78-9d99-4e4c-b35e-fea046f9fc30" />

### 7. Risk Level Segmentation
Customer were classified into Low, Medium, and High Risk
<img width="825" height="798" alt="{F2566048-67B8-4F69-941F-518129EEB82C}" src="https://github.com/user-attachments/assets/ae77aa39-6d3f-4d3c-98eb-a73fd9ba92dc" />

### 8. Risk & Pricing Analysis
- Average Charges by Risk Level
  <img width="827" height="660" alt="{773B0884-DD85-4218-A0CA-82685B31A8AA}" src="https://github.com/user-attachments/assets/d0363be5-0cc4-49a5-ac1b-dce1589836e0" />

  High risk customers generate significanly higher insurance charges compared to other risk categories. This indicated that the developed risk scoring successfully represents customer risk levels toward insurance costs.

- Average Charges by Smoker Status
  <img width="827" height="586" alt="{98A28D81-F8B4-4DE3-82F6-2D174E17EDDC}" src="https://github.com/user-attachments/assets/0e10ab0a-1d71-4028-9d3b-6ea4505a79cd" />

  Smoker customers generate insurance charges almost 4 times higher than non smokers, indicated that smoking status becomes the most important factor affecting insurance pricing.

- Average Charge by BMI Category
  <img width="829" height="678" alt="{8D4D7A6B-03AB-418B-8C85-81D323681367}" src="https://github.com/user-attachments/assets/4f55646a-2103-4229-b05f-aeab824da82e" />

  Customers in the obese BMI category generate the highest average insurance charges, indicating higher potential health risks.

- Average Charges by Age Categories
  <img width="831" height="699" alt="{0FB531D2-4152-4965-B51F-C2EEF807B7A4}" src="https://github.com/user-attachments/assets/e2a7e1c6-4a6c-4fd9-a48b-5c07db35e94b" />

  Insurance charges tend to increace in older age groups.

## Key Findings
- Smoking status has the strongest influence on insurance charges.
- High risk customers generate the highest medical insurance costs.
- Insurance charges tend to increase with age and BMI category.
- Risk scoring succesfully segments customer based on insurance risk levels.

## Business Recommendation
- Smoking status should be considered as a primary factor in insurance premium evaluation.
- Risk segmentation can support premium pricing strategy development.
- High risk customers may require adjusted premium pricing consideration.
