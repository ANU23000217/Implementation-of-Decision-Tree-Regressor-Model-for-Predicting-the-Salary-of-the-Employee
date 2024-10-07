# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1: Import the required libraries.

Step 2: Upload the csv file and read the dataset.

Step 3: Check for any null values using the isnull() function.

Step 4: From sklearn.tree inport DecisionTreeRegressor.

Step 5: Import metrics and calculate the Mean squared error.

Step 6: Apply metrics to the dataset, and predict the output.
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: ANU RADHA N
RegisterNumber:  212223230018
*/
```

```
import pandas as pd
data= pd.read_csv("C:/Users/admin/Desktop/INTR MACH/Salary.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]= le.fit_transform(data["Position"])
data.head()
x=data[["Position" , "Level"]]
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train , x_test , y_train , y_test = train_test_split(x,y,test_size=0.2 , random_state= 100)
from sklearn.tree  import DecisionTreeRegressor
dt= DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred= dt.predict(x_test)
from sklearn import metrics
mse = metrics.mean_squared_error(y_test , y_pred)
mse
r2= metrics.r2_score(y_test, y_pred)
r2
dt.predict([[5,6]])

```

## Output:

![image](https://github.com/user-attachments/assets/6730d1dc-4ed0-433e-bfb8-8f3fa176819d)
### Mean Squared Error:

![image](https://github.com/user-attachments/assets/94a419ed-01af-46e2-accf-6369ab566bcd)


![image](https://github.com/user-attachments/assets/5f9e0fa5-a67f-4a04-959d-8f70a0df96de)

![image](https://github.com/user-attachments/assets/6b36bf19-bee4-4491-8029-c6407e947feb)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
