# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Vignesh S
RegisterNumber: 212224110061 
'''

import sys

n = int(input())

a = [[0]*(n+1) for _ in range(n)]
x = [0]*n

for i in range(n):
    for j in range(n+1):
        a[i][j] = float(input())


for i in range(n):
    if a[i][i] == 0.0:
        sys.exit("Divide by zero detected!")

    for j in range(i+1, n):
        ratio = a[j][i] / a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]

for i in range(n-1, -1, -1):
    x[i] = a[i][n]
    for j in range(i+1, n):
        x[i] -= a[i][j] * x[j]
    x[i] = x[i] / a[i][i]

for i in range(n):
    print("X%d = %.2f " % (i, x[i]), end="")

```

## Output:

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

