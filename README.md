# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1: Import libraries (pandas, numpy, matplotlib).
Step 2: Load dataset and extract R&D Spend & Profit.
Step 3: Normalize feature X.
Step 4: Initialize parameters m, b, learning rate, epochs.
Step 5: Apply gradient descent updates for m and b.
Step 6: Print final slope & intercept.
Step 7: Plot scatter points and regression line.

## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: D.R.Guru Prasad
RegisterNumber:  212225040104

import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

data=pd.read_csv("Startup.csv")

X=data['R&D Spend'].values
y=data['Profit'].values

X=(X-X.mean())/X.std()

m=0
b=0
learning_rate=0.01
epochs=1000
n=len(X)

for i in range(epochs):
    y_pred=m*X+b
    dm=-(2/n)*np.sum(X*(y-y_pred))
    db=-(2/n)*np.sum(y-y_pred)
    
    m=m-learning_rate*dm
    b=b-learning_rate*db
    
print("Slope(m):",m)
print("Intercept(b):",b)
y_pred=m*X+b

plt.scatter(X,y)
plt.plot(X,y_pred)
plt.xlabel("R&D spend(normalized)")
plt.ylabel("Profit")
plt.title("Gradient Desent on 50_Startup Dataset")
plt.show()


*/
```

## Output:
![linear regression using gradient descent](sam.png)
<img width="892" height="633" alt="image" src="https://github.com/user-attachments/assets/8abd12d2-e908-4b79-8a69-279b36bc903f" />

​


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
