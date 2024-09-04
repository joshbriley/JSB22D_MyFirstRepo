# Homework Report

## Personal Details
**Name:** Josh Briley  
**Date:** September 9, 2024  
**Course:** ISC 4221: Discrete Algorithms for Science Applications  
**Instructor:** Olmo S. Zavala Romero

## Homework Questions and Answers

#### Answer to Question 1
[Insert a description for the first answer here]

```python
def myrec(x):
    if x >= 0:
        if x > 0:
            return 2 * x - myrec(x-1)
        elif x == 0:
            return 0
    else:
        return 'Input must be greater than 0'

x = int(input('Enter an integer greater than 0: '))
print(myrec(x))
```

#### Answer to Question 2
[Insert a description for the second answer here]

```python
import os

def basic_io(path):
    fileFolder = []
    if not os.path.exists(path):
        return 'Folder does not exist.'

    
    files = os.listdir(path)
    
    for i in files:
        full_path = os.path.join(path, i)
        if os.path.isdir(full_path):
            fileFolder.append('folder')
        elif os.path.isfile(full_path):
            fileFolder.append('file')
    
    output = {
        'number_files': len(files),
        'files': files,
        'fileFfolder': fileFolder
    }
    
    return output

path = str(input('Input the path to your directory: '))
print(basic_io(path))
```

#### Question 3
[Insert a description for the second answer here]

```python

import numpy as np

def add2and3(A):
    [row,col] = A.shape
    if row < 2 or col < 3:
        return 'Matrix is not the correct  dimensions. '
    secondRow = A[1,:]
    thirdCol = A[:,2]
    combination = np.hstack((secondRow,thirdCol))
    summation = sum(combination)
    return summation

A = np.array([[1, 2, 3,1],
              [4, 5, 6,1],
              [7, 8, 9,1]])

B = np.array([[1, 2],
              [4, 5],
              [7, 8]])

print(add2and3(B))

```

#### Question 4
[Insert a description for the second answer here]

```python
import numpy as np

def squareme(A, row_int):
    [num_of_rows,num_of_cols] = A.shape
    if row_int >= num_of_rows or row_int < 0:
        return 'Row not found'
    else:
        row = A[row_int,:]
        row2 = row*row
        return row2

A = np.array([[1, 2, 3],
              [4, 5, 6],
              [7, 8, 9]])
row_int = -2
print(squareme(A,row_int))

```

#### Question 5
[Insert a description for the second answer here]

```python
import matplotlib.pyplot as plt
import matplotlib
import matplotlib.animation as animation
import numpy as np

#%%%------------ data -----------
n = 100
x = np.linspace(0,2*np.pi,n)
y = np.sin(x)

#%% ------------ plot line -----------
fig, ax = plt.subplots(1,1,figsize=(10,10))
ax.set_title('Basic Plot')
ax.plot(x,y, 'r', label='1')
ax.plot(x,y+.5, 'g--', label='2')
ax.set_xlabel("Sopas")
ax.set_ylabel("Pericon")
ax.legend()
plt.show()

#%% ------------ plot scatter -----------
fig, ax = plt.subplots(1,1,figsize=(10,10))
ax.scatter(x,y, label='simplest')
ax.scatter(x,y-.3, color='b', alpha=np.linspace(0,1,len(x)), label='alpha')    # alpha
ax.scatter(x,y-.5, c=np.linspace(0,1,len(x)), label='color')                   # color
ax.scatter(x,y-.8, s=np.linspace(0,100,len(x)), label='size')                 # Size
ax.set_title("Scatter")
ax.legend()
plt.show()
```

## Additional Comments or Notes

[Include any additional comments or notes here, if any.]

---

## References (if applicable)

- [Reference 1]
- [Reference 2]
- [Etc.]
