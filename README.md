# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Detect File Encoding: Use chardet to determine the dataset's encoding.
2.Load Data: Read the dataset with pandas.read_csv using the
detected encoding. 3.Inspect Data: Check dataset structure with .info() and missing values with .isnull().sum(). 
4.Split Data: Extract text (x) and labels (y) and split into training and test sets using train_test_split. 
5.Convert Text to Numerical Data: Use CountVectorizer to transform text into a sparse matrix. 
6.Train SVM Model: Fit an SVC model on the training data.
7.Predict Labels: Predict test labels using the trained SVM model.
8.Evaluate Model: Calculate and display accuracy with metrics.accuracy_score. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: JANSI RANI A A
RegisterNumber:  212224040130


import pandas as pd
data=pd.read_csv("spam.csv", encoding='Windows-1252')
data

data.shape

x=data['v2'].values
y=data['v1'].values
x.shape

y.shape

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2, random_state=0)
x_train

x_train.shape

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn.metrics import accuracy_score,confusion_matrix,classification_report
acc=accuracy_score(y_test,y_pred)
acc

con=confusion_matrix(y_test,y_pred)
print(con)

cl=classification_report(y_test,y_pred)
print(cl)

*/
```

## Output:
## data
<img width="950" height="625" alt="image" src="https://github.com/user-attachments/assets/18270f25-bef0-44ba-9060-dc64cc64bf8c" />



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
