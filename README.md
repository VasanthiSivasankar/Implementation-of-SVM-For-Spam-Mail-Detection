# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1) Import dataset using chardet
2) Get the dataset info and check for null values
3) Assign x and y values
4) Split it into train and test data
5) Import count vectorizer and transform x_train and x_test as vectors
6) Import SVC and fit it to data
7) Find y_predict values and accuracy
## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Vasanthi Sivasankar
RegisterNumber:  212223040234
*/
```
```
import pandas as pd 
data= pd.read_csv("C:/Users/admin/Desktop/INTR MACH/spam.csv", encoding= "Windows-1252") 
data.head()
data.info()
data.isnull().sum()
x=data["y1"].values 
y=data["v2"].values 
from sklearn.model_selection import train_test_split 
x_train,x_test, y_train, y_test = train_test_split(x,y, test_size=0.2, random_state=0) 
from sklearn.feature_extraction.text import CountVectorizer 
cv=CountVectorizer()
x_train = cv.fit_ transform(x_train) 
x_test= cv.transform(x_test) 
from sklearn.svm import SVC 
svc=SVC0 svc.fit(_train,y_train) 
y_pred=svc.predict(x_test) 
y_pred 
from sklearn import metrics accuracy= metrics.accuracy_score(y_test,y_pred)
accuracy
from sklearn.metrics import confusion_matrix,classification_report
con= confusion_matrix(y_test,y_pred)
print(con)cl=classification_report(y_test,y_pred)
print(cl)
```

## Output:
![image](https://github.com/user-attachments/assets/7c41cfc4-9882-4068-8eb0-d44681815ec4)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
