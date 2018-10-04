
# Solving a Linear System


```python
import numpy as np

A = np.array([[1,2],[3,4]])
B = np.array([1,2])
```


```python
x = np.linalg.inv(A).dot(B)
x
```




Output:

array([  2.22044605e-16,   5.00000000e-01])



##### Insted we use a function given in numpy


```python
x = np.linalg.solve(A,B)
x
```


Output:

array([ 0. ,  0.5])


