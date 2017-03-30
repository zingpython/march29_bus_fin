

```python
import numpy as np
import pandas as pd
```


```python
s = pd.Series(np.random.randn(5), index=['a', 'b', 'c', 'd', 'e'])
```


```python
s
```




    a   -0.584655
    b   -0.378314
    c    1.242146
    d   -0.592002
    e   -0.183341
    dtype: float64




```python
s*(-1)
```




    a    0.584655
    b    0.378314
    c   -1.242146
    d    0.592002
    e    0.183341
    dtype: float64




```python
s[0]
```




    -0.5846551590666671




```python
s[:3]
```




    a   -0.584655
    b   -0.378314
    c    1.242146
    dtype: float64




```python
s[2:3]
```




    c    1.242146
    dtype: float64




```python
s[[4, 3, 1]]
```




    e   -0.183341
    d   -0.592002
    b   -0.378314
    dtype: float64




```python
s+20
```




    a    19.415345
    b    19.621686
    c    21.242146
    d    19.407998
    e    19.816659
    dtype: float64




```python

```
