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
```
Developed by : Karthikeyan P
Register no: 212223230102
```
```py
import numpy as np 
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
Xmean=np.mean(X)
Ymean=np.mean(Y)
num,den=0,0
for i in range(len(X)):
    num+=(X[i]-Xmean)*(Y[i]-Ymean)
    den+=(X[i]-Xmean)**2
slope=num/den
b=Ymean-slope*Xmean
ypred=slope*X + b
print("Slope is",slope,"value is",ypred)
plt.scatter(X,Y,color='red')
plt.plot(X,ypred,color='blue')
plt.show()
```
## Output
![image](https://github.com/karthikeyanpachiyappan/Univariate-Linear-Regression/assets/155143878/358b4622-39c8-4df1-abb3-22c448561169)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
