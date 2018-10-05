
# Joins


```python
import pandas as pd
import numpy as np

t1 = pd.read_csv("Datasets/table1.csv")
t2 = pd.read_csv("Datasets/table2.csv")
```


```python
t1
```



Output:

<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>user_id</th>
      <th>email</th>
      <th>age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>alice@gmail.com</td>
      <td>20</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>bob@gmail.com</td>
      <td>25</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>carol@gmail.com</td>
      <td>30</td>
    </tr>
  </tbody>
</table>
</div>




```python
t2
```


Output:

<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>user_id</th>
      <th>ad_id</th>
      <th>click</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>5</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>3</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>3</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>3</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>3</td>
      <td>4</td>
      <td>0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>3</td>
      <td>5</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
m = pd.merge(t1,t2, on ='user_id')
m
```



Output:

<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>user_id</th>
      <th>email</th>
      <th>age</th>
      <th>ad_id</th>
      <th>click</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>alice@gmail.com</td>
      <td>20</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>alice@gmail.com</td>
      <td>20</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>alice@gmail.com</td>
      <td>20</td>
      <td>5</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>bob@gmail.com</td>
      <td>25</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>bob@gmail.com</td>
      <td>25</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2</td>
      <td>bob@gmail.com</td>
      <td>25</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>3</td>
      <td>carol@gmail.com</td>
      <td>30</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>3</td>
      <td>carol@gmail.com</td>
      <td>30</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>3</td>
      <td>carol@gmail.com</td>
      <td>30</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>3</td>
      <td>carol@gmail.com</td>
      <td>30</td>
      <td>4</td>
      <td>0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>3</td>
      <td>carol@gmail.com</td>
      <td>30</td>
      <td>5</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
t1.merge(t2, on = 'user_id')
```

Output:

<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>user_id</th>
      <th>email</th>
      <th>age</th>
      <th>ad_id</th>
      <th>click</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>alice@gmail.com</td>
      <td>20</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>alice@gmail.com</td>
      <td>20</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>alice@gmail.com</td>
      <td>20</td>
      <td>5</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>bob@gmail.com</td>
      <td>25</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>bob@gmail.com</td>
      <td>25</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2</td>
      <td>bob@gmail.com</td>
      <td>25</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>3</td>
      <td>carol@gmail.com</td>
      <td>30</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>3</td>
      <td>carol@gmail.com</td>
      <td>30</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>3</td>
      <td>carol@gmail.com</td>
      <td>30</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>3</td>
      <td>carol@gmail.com</td>
      <td>30</td>
      <td>4</td>
      <td>0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>3</td>
      <td>carol@gmail.com</td>
      <td>30</td>
      <td>5</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>


