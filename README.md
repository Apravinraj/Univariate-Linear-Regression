# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![image](https://github.com/Apravinraj/Univariate-Linear-Regression/assets/118707879/b31711cc-0541-49d7-9497-c7a38f82e1fe)

4.	Compute the y -intercept of the line by using the formula:
![image](https://github.com/Apravinraj/Univariate-Linear-Regression/assets/118707879/8b42f786-7e32-44c3-b827-5f72840637aa)
  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```

Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Pravin raj.A
Register number: 212222240079
import numpy as np
import matplotlib.pyplot as py
x=np.array(eval(input()))
y=np.array(eval(input()))
x_mean=np.mean(x)
y_mean=np.mean(y)
num,denom=0,0
for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    denom+=(x[i]-x_mean)**2
m=num/denom
b=y_mean-(m*x_mean)
print(m,b)
y_pred=(m*x)+b
print(y_pred)
py.scatter(x,y,color='blue')
py.plot(x,y_pred,color='#CD5555')
py.show()

```
## Output
![image](https://github.com/Apravinraj/Univariate-Linear-Regression/assets/118707879/d22c3cbe-1ed6-4c92-a222-51404b7fcd01)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
