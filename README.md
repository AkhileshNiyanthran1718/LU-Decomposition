# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.fix a row i
2. move across columns j from i to n-1
3.for each element:
  multiply corresponding values L and U
  Add them(summation)
  subtract from A[i][j]
4.store result in U[i][j]

## Program:
(i) To find the L and U matrix
```
/*
Program to find the L and U matrix.
Developed by: D AKHILESH NIYANTHRAN
RegisterNumber: 212225220006
*/
```
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"

import numpy as np  
from scipy.linalg import lu
matrix = eval(input())
P,L,U = lu(matrix)
print(L)
print(U)
(ii) To find the LU Decomposition of a matrix
```
/*
Program to find the LU Decomposition of a matrix.
Developed by: D AKHILESH NIYANTHRAN
RegisterNumber: 212225220006
*/
```
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"

import numpy as np
from scipy.linalg import lu

A = np.array(eval(input()))
b = np.array(eval(input()))
P,L,U = lu(A)

y = np.linalg.solve(L, np.dot(P, b))
x = np.linalg.solve(U, y)

print(x)

## Output:

<img width="1491" height="744" alt="image" src="https://github.com/user-attachments/assets/4ef55ec1-8286-405c-a993-75feba336f74" />

<img width="1467" height="937" alt="image" src="https://github.com/user-attachments/assets/fa4f5873-74d0-4ffc-895e-893a76081649" />


## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

