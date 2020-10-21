---
description: get data as Dataframe from yahoo
---

# Yahoo

## Stock

Get stock data

### Basic

```python
naas_drivers.yahoo().stock("TSLA")
```

### Date

```python
date_from = -30 # Date can be number or date or today
date_to = "today"
naas_drivers.yahoo().stock("TSLA", date_from=date_from, date_to=date_to)
```

### Interval

```python
naas_drivers.yahoo().stock("TSLA", interval="1d")
```

### Moving average

```python
ma = [20,50] # max two value
naas_drivers.plot().stock("TSLA", moving_averages=ma)
```

