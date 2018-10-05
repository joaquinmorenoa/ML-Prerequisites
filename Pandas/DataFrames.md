
# DataFrames

We will use Pandas' 'read' functions. As we'll see, the data type of X is dataframe.


```python
import pandas as pd
import numpy as np

X = pd.read_csv(" Datasets/data_2d.csv ", header=None)

print(type(X))
```

Output:

<class 'pandas.core.frame.DataFrame'>
    

We'll use the info function, this gives information about the dataframe. In the dttype, pandas will try to use the most relevant data ype possible.


```python
X.info()
```
Output:

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 100 entries, 0 to 99
    
Data columns (total 3 columns):
    
0    100 non-null float64
    
1    100 non-null float64
    
2    100 non-null float64
    
dtypes: float64(3)
    
memory usage: 2.4 KB
    
    

The head() will by default give first three rows, if we need specifit number of rows then pass the argument to the head().


```python
X.head()
```




<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>17.930201</td>
      <td>94.520592</td>
      <td>320.259530</td>
    </tr>
    <tr>
      <th>1</th>
      <td>97.144697</td>
      <td>69.593282</td>
      <td>404.634472</td>
    </tr>
    <tr>
      <th>2</th>
      <td>81.775901</td>
      <td>5.737648</td>
      <td>181.485108</td>
    </tr>
    <tr>
      <th>3</th>
      <td>55.854342</td>
      <td>70.325902</td>
      <td>321.773638</td>
    </tr>
    <tr>
      <th>4</th>
      <td>49.366550</td>
      <td>75.114040</td>
      <td>322.465486</td>
    </tr>
  </tbody>
</table>
</div>




```python
X.head(10)
```




<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>17.930201</td>
      <td>94.520592</td>
      <td>320.259530</td>
    </tr>
    <tr>
      <th>1</th>
      <td>97.144697</td>
      <td>69.593282</td>
      <td>404.634472</td>
    </tr>
    <tr>
      <th>2</th>
      <td>81.775901</td>
      <td>5.737648</td>
      <td>181.485108</td>
    </tr>
    <tr>
      <th>3</th>
      <td>55.854342</td>
      <td>70.325902</td>
      <td>321.773638</td>
    </tr>
    <tr>
      <th>4</th>
      <td>49.366550</td>
      <td>75.114040</td>
      <td>322.465486</td>
    </tr>
    <tr>
      <th>5</th>
      <td>3.192702</td>
      <td>29.256299</td>
      <td>94.618811</td>
    </tr>
    <tr>
      <th>6</th>
      <td>49.200784</td>
      <td>86.144439</td>
      <td>356.348093</td>
    </tr>
    <tr>
      <th>7</th>
      <td>21.882804</td>
      <td>46.841505</td>
      <td>181.653769</td>
    </tr>
    <tr>
      <th>8</th>
      <td>79.509863</td>
      <td>87.397356</td>
      <td>423.557743</td>
    </tr>
    <tr>
      <th>9</th>
      <td>88.153887</td>
      <td>65.205642</td>
      <td>369.229245</td>
    </tr>
  </tbody>
</table>
</div>


