# EXP-6 Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

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
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: C.SHRENIDHI
RegisterNumber: 212223040196
```

```
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



# data.head()
<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/1dde3089-f94c-4d34-908e-e7191f218a0d)

<br>
<br>

# data.info()
<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/7d02284a-5a59-4a1b-99de-d850ab4774c0)

<br>
<br>

# data.isnull().sum()
<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/cdfce366-4063-4aa1-9127-afb961b47fdf)

<br>
<br>

# data['left'].value_counts()
<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/ce5cf10e-beee-4370-8e06-7fea0e66e458)

<br>
<br>


# data['salary']=le.fit_transform(data['salary'])
<br>
data.head()
<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/b3c67b9a-2f39-4c97-9d07-4b46016f37d9)

<br>
<br>

# x data
<br>
x.head()
<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/b7e7fbc0-4130-47f1-af5b-4e633d3ff6a2)

<br>
<br>

# y data
<br>
y.head()
<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/1c6a1fc0-520b-438f-b342-14b38b9800b8)

<br>
<br>

# y pred
<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/246765ac-621b-42b1-aa57-f57702c323bc)
<br>

# accuracy
<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/155261096/f6ea4eee-0c00-424c-879a-356bbede5592)

<br>
<br>


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
