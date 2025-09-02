# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First,we want to import numpy,then import sys,assume a variable.
2. For gaussian elimination method, we want to make 2nd and 3rd column zero.
3.For that we want to make a range accorting to our program output.
4.Then print the program with correct form then the output will display.


## Program:
Program to solve a matrix using Gaussian elimination without partial pivoting.
```
Developed by: Sanjay S
RegisterNumber: 212224110047

import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)

for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
        
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1, n):
        ratio = a[j][i] / a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]
            
x[n-1] = a[n-1][n] / a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    for j in range(i+1,n):
        x[i] = x[i] - a[i][j] * x[j]
    x[i] = x[i] / a[i][i]
        
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end =' ')

```
## Output:
![gaussian elimination]()
<img width="1237" height="750" alt="image" src="https://github.com/user-attachments/assets/f5130f8a-029f-417a-9bb0-f3451c306959" />
<img width="1237" height="583" alt="image" src="https://github.com/user-attachments/assets/00a9bbef-394f-47b8-8934-ac3858f30940" />




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

