# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.1.Import the necessary python packages using import statements. 
2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head(). 
3.Split the dataset using train_test_split.
4.Calculate Y_Pred and accuracy. 
5.Print all the outputs.
6.End the Program. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Durga v
RegisterNumber:  212223230052
*/
```
```
import pandas as pd
data=pd.read_csv("spam.csv",encoding='Windows-1252')
data.head()
```

## Output:
![image](https://github.com/user-attachments/assets/5c35a834-2dd1-4aa1-9f72-01540c69f5d8)

```
data.info()
```
![image](https://github.com/user-attachments/assets/e24041f1-e344-4205-8fc6-d4888dc2f901)
```
data.isnull().sum()
```
![image](https://github.com/user-attachments/assets/67c5da0e-2239-4ff2-a2bd-a94cd3cff0a9)
```
x=data['v2'].values
y=data['v1'].values
y.shape
```
![image](https://github.com/user-attachments/assets/e07fac2e-33b8-4b3d-b2a1-d14b4ebdf5b0)

```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
x_train.shape
```
![image](https://github.com/user-attachments/assets/b74f3c9b-3022-4eb1-8996-55092214381c)
```
x_test.shape
```
![image](https://github.com/user-attachments/assets/33dbeea0-3b1a-44a1-a50e-09d0104376b1)

```
y_train.shape
```
![image](https://github.com/user-attachments/assets/3efb9be6-11ea-4d6a-b8b5-cba7bedc5db5)
```
y_test.shape
```
![image](https://github.com/user-attachments/assets/42bbe91a-0960-49b5-8be7-8ea98e80d8b1)
```
from sklearn.feature_extraction.text import CountVectorizer
cv=Count
Vectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
x_train.shape
```
![image](https://github.com/user-attachments/assets/f27dfaf7-49ae-47e1-8b4b-b9893e18a99f)
```
x_test.shape
```
![image](https://github.com/user-attachments/assets/0fb5f1a4-ac81-47a5-87cb-68276b2a15b0)
```
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
```
![image](https://github.com/user-attachments/assets/c527497a-a998-409b-9be3-d1e22cec76d7)
```
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```
![image](https://github.com/user-attachments/assets/30ce5993-ccd7-464c-90ea-228df10a4794)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
