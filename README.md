# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Gather a labeled dataset containing both spam and non-spam emails, with labels typically as 0 (non-spam) and 1 (spam)
2. Clean the email text by removing punctuation, converting text to lowercase, and removing stop words to reduce noise.
3. Split the dataset into training and testing sets, typically using an 80-20 or 70-30 ratio.
4. Train the SVM on the training data, allowing it to learn patterns associated with spam and non-spam emails.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: DHARSHAN D
RegisterNumber: 212223230045 
*/
```
```
import pandas as pd
data=pd.read_csv("spam.csv",encoding='Windows-1252')
data.head()
data.tail()
data.info()
data.isnull().sum()
x=data['v2'].values
y=data['v1'].values
y.shape
x.shape
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
x_train.shape
y_train.shape
x_test.shapefrom sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
x_train = cv.fit_transform(x_train)  
x_test = cv.transform(x_test)
x_train.shape
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
x_train.shapex_train.shape
```


## Output:
![image](https://github.com/user-attachments/assets/169fec4a-a86b-4504-9b3d-e7b2738b168b)

![image](https://github.com/user-attachments/assets/2b903aa2-7226-42c2-afae-03b12ebcbc65)

![image](https://github.com/user-attachments/assets/5d6c9720-b536-496b-9d8d-8c201dab4002)

![image](https://github.com/user-attachments/assets/d6994dbd-4c5f-4df5-8845-99a68656b101)

![image](https://github.com/user-attachments/assets/dba52b05-04e6-4fd6-b7d9-c965d651cece)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
