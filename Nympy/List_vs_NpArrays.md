# Lists vs Numpy Arrays

Numpy arrays acts as vectos, which are useful in manipulating the elements in a much easier way.

```
import numpy as np

L = [1,2,3]
A = np.array([1,2,3])

for e in L:
    print (e)

for e in A:
    print (e)
```
Output: 
1

2

3

1

2

3

As we can see, the list and array has the same values.

```
L.append(4)
L = L + [5]
L2 = []

for e in L:
    L2.append(e+e)
L2
```
Output:

[2, 4, 6, 8, 10]

To add an element in the list, we use append() or addition. 

But if we want to add one element to itself we have to do it via an iteration.

```
A + A
```
Output:

array([2, 4, 6])

```
2*A
```
Output:

array([2, 4, 6])

Whereas, this isn't the case in numpy arrays. These arrays work as vectors, matrix and vector operations is much easier.

```
2*L
```
Output:

[1, 2, 3, 4, 5, 1, 2, 3, 4, 5]

```
L2 = []
for e in L:
    L2.append(e*e)
L2
```
Ouptut:
 
[1, 4, 9, 16, 25]
 
```
A**2
```
Output:

array([1, 4, 9])
 
```
np.sqrt(A)
```
Output:

array([ 1.        ,  1.41421356,  1.73205081])
```
np.log(A)
```
Output:

array([ 0.        ,  0.69314718,  1.09861229])
```
np.exp(A)
```
Output:

array([  2.71828183,   7.3890561 ,  20.08553692])
