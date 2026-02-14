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
#Preprocessing input data
import numpy as np
import matplotlib.pyplot as plt
X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(X,Y)
plt.show()

#Building the model

X_mean=np.array(X)
Y_mean=np.array(Y)

num = 0
den = 0
for i in range(len(X)):
    num += (X[i] - X_mean)*(Y[i] - Y_mean)
    den += (X[i] - X_mean)**2

m = num/den
c = Y_mean - m*X_mean

print(m, c)

#Making predications

Y_pred = m*X+c
print(Y_pred)

plt.scatter(X,Y)
plt.plot([min(X), max(X)],[min(Y_pred), max(Y_pred)],color='red')
plt.show()


```
## Output
<img width="761" height="716" alt="Screenshot 2026-02-14 092049" src="https://github.com/user-attachments/assets/468a288b-273e-4841-b22a-cd7ae42d9e61" />
<img width="1082" height="446" alt="Screenshot 2026-02-14 092113" src="https://github.com/user-attachments/assets/a726d499-5c4e-4ca4-99d5-a283dd49afa7" />
<img width="974" height="725" alt="Screenshot 2026-02-14 092127" src="https://github.com/user-attachments/assets/4719f64c-4a4a-443c-950d-f25c01f450b4" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
