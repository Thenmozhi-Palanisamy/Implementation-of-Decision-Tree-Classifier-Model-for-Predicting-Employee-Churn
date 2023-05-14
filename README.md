# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas library to read csv or excel file.
2. Import LabelEncoder using sklearn.preprocessing library.
3. .Transform the data's using LabelEncoder.
4. Import decision tree classifier from sklearn.tree library to predict the values.
5.  Find accuracy.
6.   Predict the values.
7.    End of the progra


## Program:
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Thenmozhi P
RegisterNumber:  212221230116
*/


import pandas as pd
data=pd.read_csv("Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])

## Output:
HEAD :
![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/95198708/fc49a355-2107-4abc-8d5b-a17fe390759a)

INFO:
![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/95198708/3933d17c-0ae0-41f1-96d3-ad8499bb883e)

ISNULL:
![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/95198708/c353605d-a95c-416b-8b89-2ced700b532c)

Head using labelencoder:
![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/95198708/0ad84719-6381-426c-bfb1-14bdbcf30aaa)

Accuracy with entropy::
![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/95198708/0e3956ec-dfb3-441f-8e9a-e0a2fc33df5d)

Prediction with entropy:
![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/95198708/7b900774-6ee1-4908-a47a-aa6519cec78b)

Accuracy without entropy:
![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/95198708/a5ab47bc-d578-4735-91c9-77ea16c94a6d)

Prediction without entropy:
![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/95198708/6e4a7388-47e7-4549-aa33-b09bd4ede958)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
