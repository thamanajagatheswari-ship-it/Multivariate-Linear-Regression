# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.

## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
   
## Algorithm:

### Step1
<br>Import pandas and linear_model from sklearn

### Step2
<br>Load the dataset from "carsemission.csv" into a DataFrame.

### Step3
<br>Assign 'Weight' and 'Volume' as features (X) and 'CO2' as the target (y).

### Step4
<br>Initialize the LinearRegression model and fit it with X and y.


### Step5
<br>Print the model coefficients and intercept.

### Step6
<br>Provide new input data (Weight: 3300, Volume: 1300) to predict and print the expected CO2 emissions.

## Program:
```
### developed by:Thamana G
### Reg no:26018758
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
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
<img width="703" height="350" alt="Screenshot 2026-11-27 092456" src="https://github.com/user-attachments/assets/9690619b-299a-492e-b0fc-2a08fb35cb6c" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
