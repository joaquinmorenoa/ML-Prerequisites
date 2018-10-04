
# Vectors and Matrices

We can visualise matrices as lists of lists:


```python
import numpy as np

M = np.array([[1,2],[3,4]])
L = [[1,2],[3,4]]
```


```python
L[0]
```



Output:

[1, 2]




```python
L[0][0]
```


Output:

1




```python
M[0][0]
```


Output:

1




```python
M[0,0]
```


Output:

1



We can make a matrix direcly as a matrix in numpy:


```python
M2 = np.matrix([[1,2],[3,4]])
M2
```


Output:

matrix([[1, 2],
            [3, 4]])



The official documentation advices not to use matrices, so we covert the matrix in an array:


```python
A = np.array(M2)
A
```


Output:

array([[1, 2],
           [3, 4]])



Doing Transpos of an array:


```python
A.T
```


Output:

array([[1, 3],
           [2, 4]])


