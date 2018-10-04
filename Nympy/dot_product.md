# Dot Product in Numpy

Let's take two arrays
```
import numpy as np

A = np.array([1,2,3])
B = np.array([3,2,1])

dot = 0 

for e,f in zip(A,B):
    dot += e*f
    
dot
```
Output:

10

But since we are using numpy arrays we can directly multiply the vectors
```
A*B
np.sum(A*B)
```
Output:

array([3, 4, 3])

10

```
(A*B).sum()
```
Output:

10

We use the dot() provided in numpy
```
np.dot(A,B)
```
Output:

10

We can call the dot() on the object itself
```
A.dot(B)
```
Output:

10

Let's now use the alternative for the dot product to find the angle between A and B, we'll calculate the magnititude first
```
amag = np.sqrt((A*A).sum())
amag
```
Output:

3.7416573867739413

```
amag = np.linalg.norm(A)
amag
```
Output:

3.7416573867739413

Now, to find the angle
```
cosangle = A.dot(B) / (np.linalg.norm(A)*np.linalg.norm(B))
cosangle
```
Output:

0.7142857142857143

```
angle = np.arccos(cosangle)
angle
```
Output:

0.77519337331036131



