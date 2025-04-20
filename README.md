
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program
```
Developed by: priyanka .R
RegisterNumber:  212223220081
```
```
import pandas as pd
data=pd.read_csv("Employee.csv")
data
```

## output

![image](https://github.com/user-attachments/assets/4169266a-d02f-4fd1-9b54-dfbd64dd8451)
```
data["left"].value_counts()
```

## output
![image](https://github.com/user-attachments/assets/a953bef0-cc92-47a6-96fc-290e60ba5179)
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
```
```
data.head()
```
## output

![image](https://github.com/user-attachments/assets/d64ea521-f773-4ea3-b764-1f8473e702d1)

```
data["salary"]=le.fit_transform(data["salary"])
data
```
## output

![image](https://github.com/user-attachments/assets/429bf5bf-580b-48d8-b675-63a26c525d99)
```
x=data[["satisfaction_level","last_evaluation","number_project","time_spend_company"]]
x.head()
```
## output
![image](https://github.com/user-attachments/assets/1ad4dcab-230f-42a2-bc8b-4e1b7b8bffe1)

```
y=data["left"]
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
```
```
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
```
```
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```
## output
![image](https://github.com/user-attachments/assets/8f67cda0-73eb-44a0-9480-01ad03a906f0)
```
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

 ## output
![image](https://github.com/user-attachments/assets/8ef721c2-8672-4dd3-b5ec-e7e23338f5cb)

## Result:
Thus the program to implement the Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.














