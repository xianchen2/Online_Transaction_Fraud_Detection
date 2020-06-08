# IEEE-CIS_Fraud_Detection

Predicting the probability that an online transaction is fraudulent, as denoted by the binary target isFraud.

**Data Source** [Kaggle](https://www.kaggle.com/c/ieee-fraud-detection/data)

## Validation Strategy
The timespan of the total data set is 365 days, where that of the training set is 182 days and that of the test set is 183 days. Thus, the validation strategy used in this project is **time-based validation**, training for the first 5 months and predicting the last month.

## EDA

## Data Processing

### **Dimension Reduction**
* Apply **PCA** to highly correlated and redundant V1-V339 features

### **Feature Selection** 
* Perform **Adversarial Validation** to find features that are important in differentiating cards as the training set and test set have different sets of cards

### **Feature Engineering** 
* **Combining features** to generate new features   
Feature A and B by themselves may not correlate with the target variable but FeatureA+B may correlate with the target variable.

* **Frequency Encoding** for categorical features  
Replace categorical values with corresponding frequency

* **Group statistics**   
For example, gourp by card1, get mean or std of ```TransactionAmt``` for each group. This can let the model know whether a row has abnormal ``TransactionAmt`` for their group.

### **Process TimeDelta Features**  
* **Normalize D columns** to prevent them from increasing by time
* Convert ```TransactionDT``` into datetime by providing a reference datetime

### **Mapping Emails to keep only email Domain**

## Model Training with **Hyperpt**
* **XGBoost**  
* **CatBoost**



