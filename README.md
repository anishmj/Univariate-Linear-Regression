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
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
~~~
Program for Univariate linear regression using the least squares method.
Developed by: Anish MJ
RegisterNumber: 212221230005
'''
import numpy as np

# Preprocessing Input data

X = np.array(eval(input()))
Y = np.array(eval(input()))


# Mean 
X_mean =np.mean(X)
Y_mean =np.mean(Y)
num=0 #for slope
denom=0 #for slope

#to find sum of (xi-x') &(yi-y') &(xi-x')^2

for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2
    
#calculate slope

m=num/denom

#calculate intercept
#(xi-x') & (yi-y')

b=Y_mean-m*X_mean
print(m,b)


#line equation

y=m*X+b

print(y)
~~~







##  Input: 
![inp](./input.jpg)

##  Output:
![output](leastsquare.png)

![output](graph.png)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
