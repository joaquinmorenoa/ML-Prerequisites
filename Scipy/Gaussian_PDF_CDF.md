
# Gaussian PDF and CDF


```python
from scipy.stats import norm
import numpy as np
```

To find probability densityof zero from teh standard normal distribution.


```python
print(norm.pdf(0))
```
    Output:
    0.398942280401
    

We might be working with a Gaussian that has a mean other than zero and a variance other than 1. We can pass those arguments into the pedia function as well.

So this is a standard deviation of 10 which corresponds to a variance of 100 and as expected this has a much more smaller probability density.


```python
norm.pdf(0, loc=5, scale=10)
```


    Output:
    0.035206532676429952



So if we have a random array

we can calculate the PTF of all the values at the same time.


```python
r = np.random.randn(10)
norm.pdf(r)
```



    Output:
    array([ 0.18623958,  0.29361567,  0.0273928 ,  0.34177809,  0.24312206,
            0.38750268,  0.28459912,  0.16446597,  0.38992088,  0.35150536])




```python
norm.logpdf(r)
```



    Output:
    array([-1.68072137, -1.22548363, -3.59747499, -1.07359362, -1.41419165,
           -0.94803251, -1.25667368, -1.80505159, -0.94181142, -1.04553031])



Cumulative distribution function:


```python
norm.cdf(r)
```



    Output:
    array([ 0.89145965,  0.78318667,  0.01031919,  0.2890519 ,  0.84019066,
            0.5953084 ,  0.79442456,  0.90844659,  0.5846807 ,  0.69257885])




```python
norm.logcdf(r)
```



    Output:
    array([-0.1148951 , -0.24438421, -4.57374972, -1.24114903, -0.17412644,
           -0.5186757 , -0.23013726, -0.09601918, -0.53668939, -0.36733319])


