# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.
2.Upload and read the dataset.
3.Check for any null values using the isnull() function.
4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
5.Find the accuracy of the model and predict the required values by importing the required module from sklearn.

## Program:
```
Program to imp
lement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: C.SHRENIDHI
RegisterNumber: 212223040196

import pandas as pd
data=pd.read_csv("/content/Employee (1).csv")
data.head()
data.info()
data.isnull().sum()
data['left'].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['salary']=le.fit_transform(data['salary'])
data.head()
x=data[['satisfaction_level','last_evaluation','number_project','average_montly_hours','time_spend_company','Work_accident','promotion_last_5years','salary']]
x.head()
y=data['left']
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion='entropy')
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0,5,0.8,260,6,0,1,2]])



```

## Output:
![decision tree classifier model](sam.png)


data.head()
<br>
<br>

<img width="879" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/da0f90d1-a11c-4aa2-8a3c-c37ddd55213b">
<br>
<br>

data.info()
<br>
<br>

<img width="307" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/fd88a2d0-8ae0-44e3-b939-f349bf4f1297">
<br>
<br>

data.isnull().sum()
<br>
<br>

<img width="170" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/f08e6e2f-6989-48e6-ab17-0af8c30e1237">
<br>
<br>

data['left'].value_counts()
<br>
<br>
<img width="163" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/f583ec74-dfb6-4f0b-809b-469ee3f3071f">
<br>
<br>


data['salary']=le.fit_transform(data['salary'])
data.head()
<br>
<br>

<img width="870" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/85b208c9-7be2-451e-87e2-5e06e41f4123">
<br>
<br>

x=data[['satisfaction_level','last_evaluation','number_project','average_montly_hours','time_spend_company','Work_accident','promotion_last_5years','salary']]
x.head()
<br>
<br>

<img width="870" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/08674ec4-e2d6-40a2-b71f-40ac0d904e6a">
<br>
<br>

y=data['left']
y.head()
<br>
<br>

<img width="870" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/996b60e4-6467-405e-82de-1dbe780f5794">
<br>
<br>

accuracy
<br>
<br>
<img width="217" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/74caa7d2-3b44-408e-b6ea-84d128231d58">
<br>
<br>


/usr/local/lib/python3.10/dist-packages/sklearn/base.py:439: UserWarning: X does not have valid feature names, but DecisionTreeClassifier was fitted with feature names
  warnings.warn(
array([1])








## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
