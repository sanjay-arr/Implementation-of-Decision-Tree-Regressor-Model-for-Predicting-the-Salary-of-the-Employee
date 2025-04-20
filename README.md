# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1.Import pandas
2.Import Decision Tree classifier
3.Fit the Data in the model
4.Fit the accuracy score
```
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: G.SANJAY
RegisterNumber:  212224230243
*/
```
```
import pandas as pd
data=pd.read_csv("/Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
```

## Output:
![image](https://github.com/user-attachments/assets/df76d7b4-8308-473a-8789-40be1218a591)

![image](https://github.com/user-attachments/assets/524fcbcc-fbca-4c14-a8eb-f86c5af54b98)

![image](https://github.com/user-attachments/assets/104c7650-3143-4403-a670-1afae0af1f1a)

![image](https://github.com/user-attachments/assets/17f1859a-1779-4967-8da3-22bb8e604eec)

![image](https://github.com/user-attachments/assets/f5214949-15c5-4a5b-b232-763ee40a9dfc)

![image](https://github.com/user-attachments/assets/a0e5ad95-2a9e-4126-a9ab-869a2d3c73bc)

![image](https://github.com/user-attachments/assets/febbb33a-4b6e-446d-8bcb-49780c77536e)

![image](https://github.com/user-attachments/assets/1c73039b-d25f-4a14-8a7d-21f95f6f943d)

![image](https://github.com/user-attachments/assets/c107adc4-0ce8-4866-903e-3804b7548212)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
