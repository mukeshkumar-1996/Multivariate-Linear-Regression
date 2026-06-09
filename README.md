## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Start and import the required libraries — pandas for data handling and linear_model from sklearn for regression.

### Step2
Load the dataset from the CSV file using pd.read_csv() and store it in a DataFrame df.

### Step3
Select features and target: Set X = [['Weight', 'Volume']] (independent variables). Set y = ['CO2'] (dependent variable).

### Step4
Create a Linear Regression model using linear_model.LinearRegression() and store it in regression

### Step5
Train the model using regr.fit(X, y) and display the model’s coefficients and intercept.

## Program:
```
#Developed by: Mukeshkumar V
#RegisterNumber: 212225230193

import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("car (1).csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)




```
## Output:

<img width="1764" height="892" alt="image" src="https://github.com/user-attachments/assets/9eb3a4a9-cadc-40f6-a83a-9c23a54853e9" />


<img width="735" height="77" alt="image" src="https://github.com/user-attachments/assets/ac6d8759-61cf-4933-a575-e6bfe407d61d" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
