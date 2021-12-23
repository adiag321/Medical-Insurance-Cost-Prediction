# Medical-Insurance-Cost-Prediction
Data source : https://www.kaggle.com/mirichoi0218/insurance

Data Definition

age: age of primary beneficiary

sex: insurance contractor gender, female, male

bmi: Body mass index, providing an understanding of body, weights that are relatively high or low relative to height,
objective index of body weight (kg / m ^ 2) using the ratio of height to weight, ideally 18.5 to 24.9

children: Number of children covered by health insurance / Number of dependents

smoker: Smoking

region: the beneficiary's residential area in the US, northeast, southeast, southwest, northwest.

charges: Individual medical costs billed by health insurance



## **Project Overview** 
• Seek insight from the dataset with Exploratory Data Analysis <br>
• Performed data processing, data engineering to prepare data before modeling <br>
• Built a model to predict Insurance Cost based on the features <br>

## **Exploratory Data Analysis**

• Feature sex, region has an almost balanced amount, meanwhile most people are non smoker & obese <br>
![image](https://user-images.githubusercontent.com/80570935/130601931-826570ec-df1d-4b85-918f-00eb740ed212.png)

• A person who smoke and have BMI above 30 tends to have a higher medical cost <br>
![image](https://user-images.githubusercontent.com/80570935/130602334-b62a7f7e-e1c8-45eb-be7d-ff752853d158.png)

• Older people who smoke have more expensive charges <br>
![image](https://user-images.githubusercontent.com/80570935/130602565-2cb73fa9-769b-4822-880e-c009d2fbef39.png)

• People who smoke and obese have the highest average charges compared to others <br>
![image](https://user-images.githubusercontent.com/80570935/130602770-c008fb2b-2041-440e-b92e-373e7cbed2ce.png)

## **Data Processing**
• Check missing value - there are none <br>
• Check duplicate value - there are 1 duplicate, will be remove <br>
• Feature engineering - make a new column `weight_status` based on BMI score <br>
• Feature transformation <br>
 Encoding `sex`, `region`, & `weight_status` <br>
 Ordinal encoding `smoker` <br>
• Modeling <br>
 Separating target & features <br>
 Splitting train & test data <br>
 Modeling using Linear Regression, Random Forest, Decision Tree, Ridge, & Lasso algorithm <br>
 Find the best algorithm <br>
 Tuning Hyperparameter <br>
 
 ## **Model Evaluation**
| Score | LinearRegression | DecisionTree | RandomForest | Ridge |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| MAE | 4305.20 | 2798.83 | 2608.55 | 4311.10 |
| RMSE | 6209.88 | 6067.50 | 4841.88 | 6238.13 |
| R2 | 0.77 | 0.78 | 0.78 | 0.86 |
| Train Accuracy | 0.74 | 1.0 | 0.97 | 0.74 |
| Test Accuracy | 0.77 | 0.78 | 0.86 | 0.77 | 
 
 ## **Conclusion**
Based on the predictive modeling, Linear Regression algorithm has the best score compared to the others, with MAE Score 4305.20, RMSE Score 6209.88, & R2 Score 0.77. Linear Regression algorithm is fit based on the train & test accuracy.
 
