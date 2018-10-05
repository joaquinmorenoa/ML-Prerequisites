
# Column Names


```python
import pandas as pd
import numpy as np

df = pd.read_csv("Datasets/international-airline-passengers.csv", engine="python", skipfooter=3)

```

See the header of columns.


```python
df.columns
```


Output:

Index(['Month', 'International airline passengers: monthly totals in thousands. Jan 49 ? Dec 60'], dtype='object')




```python
df.columns = ["Month","Passengers"]
```


```python
df.columns

```


Output:

Index(['Month', 'Passengers'], dtype='object')



Access a Column.


```python
df["Passengers"]
```


Output:

    0      112
    1      118
    2      132
    3      129
    4      121
    5      135
    6      148
    7      148
    8      136
    9      119
    10     104
    11     118
    12     115
    13     126
    14     141
    15     135
    16     125
    17     149
    18     170
    19     170
    20     158
    21     133
    22     114
    23     140
    24     145
    25     150
    26     178
    27     163
    28     172
    29     178
          ... 
    114    491
    115    505
    116    404
    117    359
    118    310
    119    337
    120    360
    121    342
    122    406
    123    396
    124    420
    125    472
    126    548
    127    559
    128    463
    129    407
    130    362
    131    405
    132    417
    133    391
    134    419
    135    461
    136    472
    137    535
    138    622
    139    606
    140    508
    141    461
    142    390
    143    432
    Name: Passengers, Length: 144, dtype: int64




```python
df.Passengers
```




    0      112
    1      118
    2      132
    3      129
    4      121
    5      135
    6      148
    7      148
    8      136
    9      119
    10     104
    11     118
    12     115
    13     126
    14     141
    15     135
    16     125
    17     149
    18     170
    19     170
    20     158
    21     133
    22     114
    23     140
    24     145
    25     150
    26     178
    27     163
    28     172
    29     178
          ... 
    114    491
    115    505
    116    404
    117    359
    118    310
    119    337
    120    360
    121    342
    122    406
    123    396
    124    420
    125    472
    126    548
    127    559
    128    463
    129    407
    130    362
    131    405
    132    417
    133    391
    134    419
    135    461
    136    472
    137    535
    138    622
    139    606
    140    508
    141    461
    142    390
    143    432
    Name: Passengers, Length: 144, dtype: int64



Insert another row.


```python
df['ones'] = 1
```


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
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1949-01</td>
      <td>112</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1949-02</td>
      <td>118</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1949-03</td>
      <td>132</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1949-04</td>
      <td>129</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1949-05</td>
      <td>121</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>


