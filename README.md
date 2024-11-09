# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1.Import the necessary python packages using import statements.
Step 2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().
Step 3.Split the dataset using train_test_split.
Step 4.Calculate Y_Pred and accuracy.
Step 5.Print all the outputs.
Step 6.End the Program.


## Program:
```
Program to implement the SVM For Spam Mail Detection..
Developed by: DHARSHAN D
RegisterNumber:  212223230045
```

```
import pandas as pd
data=pd.read_csv('spam.csv',encoding='Windows-1252')

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values
y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.35,random_state=0)

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

from sklearn.metrics import confusion_matrix, classification_report
con = confusion_matrix(y_test,y_pred)
con
cl=classification_report(y_test,y_pred)

```

## Output:
### Head:
![Screenshot 2024-10-24 090718](https://github.com/user-attachments/assets/8d5f9ec5-e9db-454e-87be-54cae7143942)

### Info:
![Screenshot 2024-10-24 090745](https://github.com/user-attachments/assets/4a481a20-c14d-45d4-bfb4-e0699d7ea4e4)

### Accuracy:
![image](https://github.com/user-attachments/assets/a9397f89-a366-4f85-9f0b-2681e8aea112)




## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
