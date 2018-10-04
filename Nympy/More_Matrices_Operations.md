
# More Matrix Operations

##### Matrix Inverse:


```python
import numpy as np

A = np.array([[1,2],[3,4]])

Ainv = np.linalg.inv(A)
Ainv
```




Output:

array([[-2. ,  1. ],
           [ 1.5, -0.5]])



##### Determinant of matrix:


```python
np.linalg.det(A)
```




Output:

-2.0000000000000004



##### Diagonal of Matrix:


```python
np.diag(A)
```



Output:

array([1, 4])



##### Make diagonal vector:


```python
np.diag([1,2])
```


Output:

array([[1, 0],
           [0, 2]])



##### Outer and inner product:


```python
a = np.array([1,2])
b = np.array([3,4])

np.inner(a,b)
```



Output:

11




```python
np.outer(a,b)
```


Output:

array([[3, 4],
           [6, 8]])



##### Matrix Trace:


```python
np.diag(A).sum()
```


Output:

5



##### Numpy gives a direct funcion:


```python
np.trace(A)
```

Output:

5



##### Eigenvectors and eigenvalues:


```python
X = np.random.rand(100,3)

voc = np.cov(X.T)
voc
```


Output:

array([[ 0.07270871,  0.00772217, -0.00301167],
           [ 0.00772217,  0.0840736 ,  0.00355129],
           [-0.00301167,  0.00355129,  0.06790438]])




```python
np.linalg.eigh(voc)
```

Output:

(array([ 0.06396443,  0.0725737 ,  0.08814856]),
     array([[-0.56564723,  0.70321624, -0.43073209],
            [ 0.34915131, -0.26896956, -0.89763508],
            [-0.74708538, -0.65813547, -0.09338699]]))


