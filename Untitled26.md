

```python
import pandas as pd
```


```python
# create Data Frame object
stocks = ["IBM", "APPLE", "TWTTR", "GE", "MSFT"]
prices = [115.00, 119.14, 19.77, 25.99, 26]
```


```python
portfolio = list(zip(stocks,prices))
print(portfolio)
```

    [('IBM', 115.0), ('APPLE', 119.14), ('TWTTR', 19.77), ('GE', 25.99), ('MSFT', 26)]



```python
df = pd.DataFrame(data=portfolio, columns=['stocks', 'prices'])
df
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>stocks</th>
      <th>prices</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>IBM</td>
      <td>115.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>APPLE</td>
      <td>119.14</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TWTTR</td>
      <td>19.77</td>
    </tr>
    <tr>
      <th>3</th>
      <td>GE</td>
      <td>25.99</td>
    </tr>
    <tr>
      <th>4</th>
      <td>MSFT</td>
      <td>26.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
#lets add another col
df['new_col'] = " "
```


```python
df
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>stocks</th>
      <th>prices</th>
      <th>new_col</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>IBM</td>
      <td>115.00</td>
      <td></td>
    </tr>
    <tr>
      <th>1</th>
      <td>APPLE</td>
      <td>119.14</td>
      <td></td>
    </tr>
    <tr>
      <th>2</th>
      <td>TWTTR</td>
      <td>19.77</td>
      <td></td>
    </tr>
    <tr>
      <th>3</th>
      <td>GE</td>
      <td>25.99</td>
      <td></td>
    </tr>
    <tr>
      <th>4</th>
      <td>MSFT</td>
      <td>26.00</td>
      <td></td>
    </tr>
  </tbody>
</table>
</div>




```python
df['new_col'] = 5
```


```python
df
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>stocks</th>
      <th>prices</th>
      <th>new_col</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>IBM</td>
      <td>115.00</td>
      <td>5</td>
    </tr>
    <tr>
      <th>1</th>
      <td>APPLE</td>
      <td>119.14</td>
      <td>5</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TWTTR</td>
      <td>19.77</td>
      <td>5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>GE</td>
      <td>25.99</td>
      <td>5</td>
    </tr>
    <tr>
      <th>4</th>
      <td>MSFT</td>
      <td>26.00</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
# access the item by loc
print(df.loc[2])
```

    stocks     TWTTR
    prices     19.77
    new_col        5
    Name: 2, dtype: object



```python
# slicing df
print(df.loc[1:3])
```

      stocks  prices  new_col
    1  APPLE  119.14        5
    2  TWTTR   19.77        5
    3     GE   25.99        5



```python
# lets write this to csv file
df.to_csv("rrr_portfolio.csv", index=True)
```


```python

```
