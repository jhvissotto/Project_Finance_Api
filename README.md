# Ecosystem

⭐ Portal:     https://bit.ly/finance_analytics  
📊 Blog:       https://slashpage.com/jh-analytics  

📈 Softrader:  https://pypi.org/project/softrader  

🐍 Python:     https://github.com/jhvissotto/Project_Finance_Api_Python  
🐍 Pypi:       https://pypi.org/project/jh-finance-api  

🟦 TScript:    https://github.com/jhvissotto/Project_Finance_Api_TScript  
🟦 NPM:        https://www.npmjs.com/package/finance-analytics-api  

🧮 PyHelpers:  https://github.com/jhvissotto/Library_Python_Helpers  

🔌 Server:     https://bit.ly/jh_finance_api  
🔌 Swagger:    https://bit.ly/jh_finance_api_swagger  



# Library

```python
!pip install jh_finance_api
```

```py
from typing import Literal as Lit
import jh_finance_api as jh
```


# Info

```py
info = jh.info.get(TICKER='MSFT')
```


# Market

```py
assert jh.market_history.PERIODS == Lit['1m','2m','5m','15m','30m','60m','90m','1h','1d','5d','1wk','1mo','3mo']
assert jh.market_history.UNTILS  == Lit['1d','5d','1mo','3mo','6mo','1y','2y','5y','10y','ytd','max']

jh.market_history.get(TICKER='MSFT', period='1mo', until='max')
```

|    | Date                |   Adj Close |   Close |   High |    Low |   Open |    Volume |
|---:|:--------------------|------------:|--------:|-------:|-------:|-------:|----------:|
|  0 | 2025-04-01 00:00:00 |     373.11  |  373.11 | 385.08 | 369.35 | 374.65 |  95966917 |
|  1 | 2025-03-01 00:00:00 |     375.39  |  375.39 | 402.15 | 367.24 | 398.82 | 491786600 |
|  2 | 2025-02-01 00:00:00 |     396.196 |  396.99 | 419.31 | 386.57 | 411.6  | 432448900 |
|  3 | 2025-01-01 00:00:00 |     414.229 |  415.06 | 448.38 | 410.72 | 425.53 | 462562700 |
|  4 | 2024-12-01 00:00:00 |     420.657 |  421.5  | 456.16 | 420.66 | 421.57 | 439902400 |



# Financials

```py
jh.financial_list.get(pages=10)
```

| Country   | Ticker   | Name              | Slug            |
|:----------|:---------|:------------------|:----------------|
| USA       | AAPL     | Apple             | apple           |
| USA       | NVDA     | NVIDIA            | nvidia          |
| USA       | MSFT     | Microsoft         | microsoft       |
| USA       | AMZN     | Amazon            | amazon          |
| USA       | GOOG     | Alphabet (Google) | alphabet-google |



```py
jh.financial_raw.get(slug='microsoft')
```

|   Year |   Shares |   Capital |   DYield |   Revenue |   Income |   Asset |   Equity |
|-------:|---------:|----------:|---------:|----------:|---------:|--------:|---------:|
|   2025 |     7430 | 2.815e+06 |     0.8  |    261800 |   113610 |  512160 |   268470 |
|   2024 |     7430 | 3.2e+06   |     0.73 |    227580 |   101210 |  411970 |   206220 |
|   2023 |     7450 | 2.794e+06 |     0.74 |    204090 |    82580 |  364840 |   166540 |
|   2022 |     7500 | 1.787e+06 |     1.06 |    184900 |    79680 |  333770 |   141980 |
|   2021 |     7550 | 2.522e+06 |     0.68 |    153280 |    60720 |  301310 |   118300 |



```py
Raw, Ratios = jh.financial_ratios.get(slug='microsoft')

print(Ratios)
```

|   N |   Year |   Cap Var |   Rev Grw |   Ast Grw |   DY |   EY |   P/S |   P/A |   Margin |   ROA |   E/A |
|----:|-------:|----------:|----------:|----------:|-----:|-----:|------:|------:|---------:|------:|------:|
|   0 |   2025 |    -12.03 |     15.04 |     24.32 | 0.81 | 4.04 | 10.75 |  5.5  |     43.4 |  22.2 |  52.4 |
|  -1 |   2024 |     14.53 |     11.51 |     12.92 | 0.73 | 3.16 | 14.06 |  7.77 |     44.5 |  24.6 |  50.1 |
|  -2 |   2023 |     56.35 |     10.38 |      9.31 | 0.74 | 2.96 | 13.69 |  7.66 |     40.5 |  22.6 |  45.6 |
|  -3 |   2022 |    -29.14 |     20.63 |     10.77 | 1.06 | 4.46 |  9.66 |  5.35 |     43.1 |  23.9 |  42.5 |
|  -4 |   2021 |     50.03 |     14.18 |      5.15 | 0.68 | 2.41 | 16.45 |  8.37 |     39.6 |  20.2 |  39.3 |