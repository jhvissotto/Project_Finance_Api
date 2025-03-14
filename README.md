# About

- Server:   https://bit.ly/jh_finance_api
- Swagger:  https://bit.ly/jh_finance_api_swagger
- Related:  https://slashpage.com/jh-analytics


# Library

```python
!pip install jh_finance_api
```

```python
import jh_finance_api as jh
```


# Financials

```python
jh.financial._list(pages=10)
```

| Country   | Ticker   | Name              | Slug            |
|:----------|:---------|:------------------|:----------------|
| USA       | AAPL     | Apple             | apple           |
| USA       | NVDA     | NVIDIA            | nvidia          |
| USA       | MSFT     | Microsoft         | microsoft       |
| USA       | AMZN     | Amazon            | amazon          |
| USA       | GOOG     | Alphabet (Google) | alphabet-google |


```python
jh.financial.raw(slug='microsoft')
```


|   Year |   Shares |   Capital |   DYield |   Revenue |   Income |   Asset |   Equity |
|-------:|---------:|----------:|---------:|----------:|---------:|--------:|---------:|
|   2025 |     7430 | 2.815e+06 |     0.8  |    261800 |   113610 |  512160 |   268470 |
|   2024 |     7430 | 3.2e+06   |     0.73 |    227580 |   101210 |  411970 |   206220 |
|   2023 |     7450 | 2.794e+06 |     0.74 |    204090 |    82580 |  364840 |   166540 |
|   2022 |     7500 | 1.787e+06 |     1.06 |    184900 |    79680 |  333770 |   141980 |
|   2021 |     7550 | 2.522e+06 |     0.68 |    153280 |    60720 |  301310 |   118300 |