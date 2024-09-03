# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by:Iswarya P 
RegisterNumber: 212223230082 
*/

import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input("Enter X value:")))
Y=np.array(eval(input("Enter Y value:")))
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0
denom=0
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2
m=num/denom
b=Y_mean-m*X_mean
print("The m value is: ",m)
print("The b value is: ",b)
y_predicted=m*X+b
print("The Y_Predicted value is: ",y_predicted)

plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.show()
```

## Output:

```
Enter X value: 8,12,21,6,15
Enter Y value: 3,10,31,6,8
The m value is:  1.6416430594900853
The b value is:  -8.75637393767706
The Y_Predicted value is:  [ 4.37677054 10.94334278 25.71813031  1.09348442 15.86827195]
```
![image](https://github.com/user-attachments/assets/1a3bb929-ed66-4b3c-a230-9fa25009cf0a)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
