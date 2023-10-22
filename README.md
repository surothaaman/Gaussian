# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import the numpy module to use the built in function for calculation. 2.Import the sys function. Get input from the user for the matrix i and j using for loop. 3.Check wheather the matrix of element is divisible by zero. If divisible by zero then print zero is detected. And further find the ratio of the matrix. 4.End the program.

## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by:SUROTHAAMAN R
RegisterNumber:23008504
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())

for i in range(n):
    if a[i][j]==0.0:
        sys.exit('Divide by zero notfound!')
    for j in range(i+1,n):
        scalar=a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k]=a[j][k]-scalar*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print("X%d = %0.2f"%(i,x[i]),end=' ')

*/
```

## Output:
![Screenshot (33)](https://github.com/surothaaman/Gaussian/assets/133313653/7acf25b0-f391-4495-be7d-d9c7873d872d)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

