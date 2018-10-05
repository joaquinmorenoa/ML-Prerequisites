
# Selecting rows and colomns


```python
import pandas as pd
import numpy as np

X = pd.read_csv("Datasets/data_2d.csv", header=None)
```

We'll use the matrix function to access the rows and colomns easily.


```python
M = X.as_matrix()
```

But if we see, even if the 


```python
print(type(M))
```
Output:

<class 'numpy.ndarray'>
    

Now, we'll see that X[0] will give us all the values in first coloumn. Whereas in numpy this gives us all the values in first row.


```python
X[0]
```



Output:

    0     17.930201
    1     97.144697
    2     81.775901
    3     55.854342
    4     49.366550
    5      3.192702
    6     49.200784
    7     21.882804
    8     79.509863
    9     88.153887
    10    60.743854
    11    67.415582
    12    48.318116
    13    28.829972
    14    43.853743
    15    25.313694
    16    10.807727
    17    98.365746
    18    29.146910
    19    65.100302
    20    24.644113
    21    37.559805
    22    88.164506
    23    13.834621
    24    64.410844
    25    68.925992
    26    39.488442
    27    52.463178
    28    48.484787
    29     8.062088
            ...    
    70    30.187692
    71    11.788418
    72    18.292424
    73    96.712668
    74    31.012739
    75    11.397261
    76    17.392556
    77    72.182694
    78    73.980021
    79    94.493058
    80    84.562821
    81    51.742474
    82    53.748590
    83    85.050835
    84    46.777250
    85    49.758434
    86    24.119257
    87    27.201576
    88     7.009596
    89    97.646950
    90     1.382983
    91    22.323530
    92    45.045406
    93    40.163991
    94    53.182740
    95    46.456779
    96    77.130301
    97    68.600608
    98    41.693887
    99     4.142669
    Name: 0, Length: 100, dtype: float64



Pandas dataframes are for 2d objcts whereas, pandas series are for 1d  objecets.


```python
print(type(X[0]))
```
Output:

<class 'pandas.core.series.Series'>
    

To get a row, we can use any of the two functions


```python
X.iloc[0]
```


Output:

    0     17.930201
    1     94.520592
    2    320.259530
    Name: 0, dtype: float64




```python
X.loc[0]
```


Output:

    0     17.930201
    1     94.520592
    2    320.259530
    Name: 0, dtype: float64




```python
print(type(X.loc[0]))
```
Output:

    <class 'pandas.core.series.Series'>
    

We can select more than one coloumn. Suppose we choose 0th and 2nd coloumn.


```python
X[[0,2]]
```


Output:

<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>17.930201</td>
      <td>320.259530</td>
    </tr>
    <tr>
      <th>1</th>
      <td>97.144697</td>
      <td>404.634472</td>
    </tr>
    <tr>
      <th>2</th>
      <td>81.775901</td>
      <td>181.485108</td>
    </tr>
    <tr>
      <th>3</th>
      <td>55.854342</td>
      <td>321.773638</td>
    </tr>
    <tr>
      <th>4</th>
      <td>49.366550</td>
      <td>322.465486</td>
    </tr>
    <tr>
      <th>5</th>
      <td>3.192702</td>
      <td>94.618811</td>
    </tr>
    <tr>
      <th>6</th>
      <td>49.200784</td>
      <td>356.348093</td>
    </tr>
    <tr>
      <th>7</th>
      <td>21.882804</td>
      <td>181.653769</td>
    </tr>
    <tr>
      <th>8</th>
      <td>79.509863</td>
      <td>423.557743</td>
    </tr>
    <tr>
      <th>9</th>
      <td>88.153887</td>
      <td>369.229245</td>
    </tr>
    <tr>
      <th>10</th>
      <td>60.743854</td>
      <td>427.605804</td>
    </tr>
    <tr>
      <th>11</th>
      <td>67.415582</td>
      <td>292.471822</td>
    </tr>
    <tr>
      <th>12</th>
      <td>48.318116</td>
      <td>395.529811</td>
    </tr>
    <tr>
      <th>13</th>
      <td>28.829972</td>
      <td>319.031348</td>
    </tr>
    <tr>
      <th>14</th>
      <td>43.853743</td>
      <td>287.428144</td>
    </tr>
    <tr>
      <th>15</th>
      <td>25.313694</td>
      <td>292.768909</td>
    </tr>
    <tr>
      <th>16</th>
      <td>10.807727</td>
      <td>159.663308</td>
    </tr>
    <tr>
      <th>17</th>
      <td>98.365746</td>
      <td>438.798964</td>
    </tr>
    <tr>
      <th>18</th>
      <td>29.146910</td>
      <td>250.986309</td>
    </tr>
    <tr>
      <th>19</th>
      <td>65.100302</td>
      <td>231.711508</td>
    </tr>
    <tr>
      <th>20</th>
      <td>24.644113</td>
      <td>163.398161</td>
    </tr>
    <tr>
      <th>21</th>
      <td>37.559805</td>
      <td>83.480155</td>
    </tr>
    <tr>
      <th>22</th>
      <td>88.164506</td>
      <td>466.265806</td>
    </tr>
    <tr>
      <th>23</th>
      <td>13.834621</td>
      <td>100.886430</td>
    </tr>
    <tr>
      <th>24</th>
      <td>64.410844</td>
      <td>365.641048</td>
    </tr>
    <tr>
      <th>25</th>
      <td>68.925992</td>
      <td>426.140015</td>
    </tr>
    <tr>
      <th>26</th>
      <td>39.488442</td>
      <td>235.532389</td>
    </tr>
    <tr>
      <th>27</th>
      <td>52.463178</td>
      <td>283.291640</td>
    </tr>
    <tr>
      <th>28</th>
      <td>48.484787</td>
      <td>298.581440</td>
    </tr>
    <tr>
      <th>29</th>
      <td>8.062088</td>
      <td>309.234109</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>70</th>
      <td>30.187692</td>
      <td>89.539008</td>
    </tr>
    <tr>
      <th>71</th>
      <td>11.788418</td>
      <td>181.550683</td>
    </tr>
    <tr>
      <th>72</th>
      <td>18.292424</td>
      <td>224.773383</td>
    </tr>
    <tr>
      <th>73</th>
      <td>96.712668</td>
      <td>219.567094</td>
    </tr>
    <tr>
      <th>74</th>
      <td>31.012739</td>
      <td>298.490216</td>
    </tr>
    <tr>
      <th>75</th>
      <td>11.397261</td>
      <td>199.944045</td>
    </tr>
    <tr>
      <th>76</th>
      <td>17.392556</td>
      <td>43.915692</td>
    </tr>
    <tr>
      <th>77</th>
      <td>72.182694</td>
      <td>256.068378</td>
    </tr>
    <tr>
      <th>78</th>
      <td>73.980021</td>
      <td>159.372581</td>
    </tr>
    <tr>
      <th>79</th>
      <td>94.493058</td>
      <td>447.132704</td>
    </tr>
    <tr>
      <th>80</th>
      <td>84.562821</td>
      <td>233.078830</td>
    </tr>
    <tr>
      <th>81</th>
      <td>51.742474</td>
      <td>131.070180</td>
    </tr>
    <tr>
      <th>82</th>
      <td>53.748590</td>
      <td>298.814333</td>
    </tr>
    <tr>
      <th>83</th>
      <td>85.050835</td>
      <td>451.803523</td>
    </tr>
    <tr>
      <th>84</th>
      <td>46.777250</td>
      <td>368.366436</td>
    </tr>
    <tr>
      <th>85</th>
      <td>49.758434</td>
      <td>254.706774</td>
    </tr>
    <tr>
      <th>86</th>
      <td>24.119257</td>
      <td>168.308433</td>
    </tr>
    <tr>
      <th>87</th>
      <td>27.201576</td>
      <td>146.342260</td>
    </tr>
    <tr>
      <th>88</th>
      <td>7.009596</td>
      <td>176.810149</td>
    </tr>
    <tr>
      <th>89</th>
      <td>97.646950</td>
      <td>219.160280</td>
    </tr>
    <tr>
      <th>90</th>
      <td>1.382983</td>
      <td>252.905653</td>
    </tr>
    <tr>
      <th>91</th>
      <td>22.323530</td>
      <td>127.570479</td>
    </tr>
    <tr>
      <th>92</th>
      <td>45.045406</td>
      <td>375.822340</td>
    </tr>
    <tr>
      <th>93</th>
      <td>40.163991</td>
      <td>80.389019</td>
    </tr>
    <tr>
      <th>94</th>
      <td>53.182740</td>
      <td>142.718183</td>
    </tr>
    <tr>
      <th>95</th>
      <td>46.456779</td>
      <td>336.876154</td>
    </tr>
    <tr>
      <th>96</th>
      <td>77.130301</td>
      <td>438.460586</td>
    </tr>
    <tr>
      <th>97</th>
      <td>68.600608</td>
      <td>355.900287</td>
    </tr>
    <tr>
      <th>98</th>
      <td>41.693887</td>
      <td>284.834637</td>
    </tr>
    <tr>
      <th>99</th>
      <td>4.142669</td>
      <td>168.034401</td>
    </tr>
  </tbody>
</table>
<p>100 rows × 2 columns</p>
</div>



We can also select specific row, suppose we want all the rows where hte data in 0th coloumn is less than 5.


```python
X[X[0]<5]
```



Output:

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
      <th>5</th>
      <td>3.192702</td>
      <td>29.256299</td>
      <td>94.618811</td>
    </tr>
    <tr>
      <th>44</th>
      <td>3.593966</td>
      <td>96.252217</td>
      <td>293.237183</td>
    </tr>
    <tr>
      <th>54</th>
      <td>4.593463</td>
      <td>46.335932</td>
      <td>145.818745</td>
    </tr>
    <tr>
      <th>90</th>
      <td>1.382983</td>
      <td>84.944087</td>
      <td>252.905653</td>
    </tr>
    <tr>
      <th>99</th>
      <td>4.142669</td>
      <td>52.254726</td>
      <td>168.034401</td>
    </tr>
  </tbody>
</table>
</div>




```python
X[0] <5

```


Output:

    0     False
    1     False
    2     False
    3     False
    4     False
    5      True
    6     False
    7     False
    8     False
    9     False
    10    False
    11    False
    12    False
    13    False
    14    False
    15    False
    16    False
    17    False
    18    False
    19    False
    20    False
    21    False
    22    False
    23    False
    24    False
    25    False
    26    False
    27    False
    28    False
    29    False
          ...  
    70    False
    71    False
    72    False
    73    False
    74    False
    75    False
    76    False
    77    False
    78    False
    79    False
    80    False
    81    False
    82    False
    83    False
    84    False
    85    False
    86    False
    87    False
    88    False
    89    False
    90     True
    91    False
    92    False
    93    False
    94    False
    95    False
    96    False
    97    False
    98    False
    99     True
    Name: 0, Length: 100, dtype: bool


