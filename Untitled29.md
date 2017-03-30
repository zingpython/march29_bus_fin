

```python
import requests
```


```python
#Creating a wrapper with requests
def company_search(ticker):
    lookup_url = "http://dev.markitondemand.com/Api/v2/Lookup/json?input="
    r = requests.get(lookup_url + ticker)
    print(r.json())
company_search("aapl")
```

    [{'Name': 'Apple Inc', 'Exchange': 'NASDAQ', 'Symbol': 'AAPL'}, {'Name': 'AAPL ALPHA INDEX', 'Exchange': 'NASDAQ', 'Symbol': 'AVSPY'}, {'Name': 'NAS OMX Alpha   AAPL vs. SPY  Settle', 'Exchange': 'NASDAQ', 'Symbol': 'AIX'}]



```python
#Creating a wrapper with requests
def get_quote(ticker):
        quote_url = "http://dev.markitondemand.com/Api/v2/Quote/json?symbol="
        r = requests.get(quote_url + ticker)
        print(r.json())
get_quote("aapl")
```

    {'ChangePercent': 0.222531293463138, 'Name': 'Apple Inc', 'Change': 0.319999999999993, 'MSDate': 42823, 'LastPrice': 144.12, 'ChangeYTD': 115.82, 'MarketCap': 756131344800, 'Volume': 29120949, 'Symbol': 'AAPL', 'ChangePercentYTD': 24.4344672768089, 'Status': 'SUCCESS', 'High': 144.49, 'Timestamp': 'Wed Mar 29 00:00:00 UTC-04:00 2017', 'Open': 143.68, 'Low': 143.19}



```python

```
