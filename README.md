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
5.Find the accuracy of the model and predict the required values by importing the required module from sklearn.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
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

*/
```

## Output
data.head()



<img width="875" alt="image" src="https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/0d3c3ed8-2685-4e1c-a07f-4c8dae9f5951">




data.info()




<img width="319" alt="image" src="https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/a07c1bd4-52a7-4c5c-b50e-d427a9f8085b">



Label Encoder on Salary



<img width="125" alt="image" src="https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/79631720-f40d-473b-ab0e-e6d251fd7eb7">
<br><br>




<img width="142" alt="image" src="https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/bf517e6f-b08a-443f-8cd6-fad25106c976">




accuracy



<img width="133" alt="image" src="https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/afcd6f87-d30d-46ed-a96d-906062b84385">

prediction aafter passing the values for attribute


<img width="878" alt="image" src="https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/afe9d828-b2f7-4877-8d89-012e8da3fe1d">








## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
