# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries (pandas, chardet, sklearn, etc.).

2.Detect the encoding of the CSV file using chardet.

3.Read the CSV file with the correct encoding.

4.Check the data for structure and missing values.

5.Split the data into input (x = messages) and output (y = labels).

6.Divide the data into training and testing sets.

7.Convert text data into numbers using CountVectorizer.

8.Train an SVM model, make predictions, and calculate accuracy.. 

## Program:
```
/*
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: SATHISH S
RegisterNumber: 212225040390

import chardet
file='spam.csv'
with open(file,'rb')as rawdata:
    result=chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv("spam.csv",encoding='windows-1252')
data.head()

data.info()

data.isnull().sum()

x=data["v2"].values
y=data["v1"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy 
*/
```

## Output:
Result output
<img width="1243" height="38" alt="596610542-2ffe12ee-a8a0-45cf-9c12-673a82726f82" src="https://github.com/user-attachments/assets/ecb88422-a06d-4964-8ff8-53c21160f838" />
data.head():
<img width="1243" height="227" alt="596610754-860bfc8e-6315-466c-bba8-29dffe54379a" src="https://github.com/user-attachments/assets/24f31105-5bb1-4310-b894-84ced7633616" />
data.info():
<img width="1231" height="257" alt="596610940-038d1d55-43af-4fb9-8674-cc680ac3ca15" src="https://github.com/user-attachments/assets/9cf4c0ce-8127-4884-813d-bf68bc9e01f2" />
data.isnull().sum():
<img width="1231" height="130" alt="596611084-94e6e5ac-7e6a-403c-a6ee-f6c901472b2c" src="https://github.com/user-attachments/assets/38e86782-e85a-4c04-a871-a594c541faae" />
y_pred:
<img width="1243" height="37" alt="596611230-e840293c-6bd1-439c-a6b0-0aa4e4231ae4" src="https://github.com/user-attachments/assets/e8008a2d-97cb-41c3-9e52-ec74b8d999aa" />
accuracy():
<img width="1243" height="38" alt="596611520-6a989139-62df-4c08-9938-f3485d5241ae" src="https://github.com/user-attachments/assets/b14b10e0-7b72-47c5-ae39-677eb0bcb5ac" />


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
