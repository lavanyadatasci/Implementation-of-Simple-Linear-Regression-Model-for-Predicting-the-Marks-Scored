# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1: Import the required libraries: numpy, matplotlib.pyplot, LinearRegression from sklearn.linear_model

2: Initialize the dataset: Assign values to independent variable X (hours studied) Assign values to dependent variable Y (marks scored)

3: Reshape the X data into a 2D array using reshape(-1,1)

4: Create the Linear Regression model: model = LinearRegression()

5: Train the model using the dataset: model.fit(X, Y)

6: Compute the slope (m) and intercept (b): m = model.coef_[0] b = model.intercept_

7: Form the regression equation: Y = mX + b

8: Accept user input for prediction: Read value of x_input (hours studied)

9: Predict the output using the model: predicted_value = model.predict([[x_input]])

10: Generate predicted values for all X: Y_pred = model.predict(X)

11: Plot the graph: Draw scatter plot for actual data points Draw regression line using predicted values

12: Display labels, title, legend and show the plot

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Lavanya A
RegisterNumber:  212225230147
*/
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression


X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])

model = LinearRegression()

model.fit(X, Y)

m = model.coef_[0]
b = model.intercept_

print("Slope (m):", m)
print("Intercept (b):", b)

x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])

Y_pred = model.predict(X)

plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()

```

## Output:
<img width="881" height="623" alt="WhatsApp Image 2026-09-02 at 22 16 12" src="https://github.com/user-attachments/assets/059b8aaa-907a-48d4-91ed-fae095bb2c62" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
