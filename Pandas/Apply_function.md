
# Apply Function

Suppose we want to derive a new column where each cell is derived from the values already in its row, we use apply function. Here, we are creating a dt column of date object.


```python
import pandas as pd
import numpy as np

df = pd.read_csv("C:/Users/dubek/Downloads/New folder/international-airline-passengers.csv", engine="python", skipfooter=3)
df.columns = ["Month","Passengers"]
df['ones'] = 1
```


```python
from datetime import datetime

datetime.strptime("1945-05","%Y-%m")
```



Output: 

datetime.datetime(1945, 5, 1, 0, 0)




```python
df['dt'] = df.apply(lambda row: datetime.strptime(row['Month'],"%Y-%m"), axis =1)
```


```python
df.info()
```
Output:
<class 'pandas.core.frame.DataFrame'>

RangeIndex: 144 entries, 0 to 143

Data columns (total 4 columns):

Month         144 non-null object

Passengers    144 non-null int64

ones          144 non-null int64

dt            144 non-null datetime64[ns]

dtypes: datetime64[ns](1), int64(2), object(1)

memory usage: 4.6+ KB
    


```python
df.head()
```



Output:

<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Month</th>
      <th>Passengers</th>
      <th>ones</th>
      <th>dt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1949-01</td>
      <td>112</td>
      <td>1</td>
      <td>1949-01-01</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1949-02</td>
      <td>118</td>
      <td>1</td>
      <td>1949-02-01</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1949-03</td>
      <td>132</td>
      <td>1</td>
      <td>1949-03-01</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1949-04</td>
      <td>129</td>
      <td>1</td>
      <td>1949-04-01</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1949-05</td>
      <td>121</td>
      <td>1</td>
      <td>1949-05-01</td>
    </tr>
  </tbody>
</table>
</div>


