---
description: Create chart easily with plotly
---

# Plotly

{% embed url="https://plotly.com/" caption="Website" %}

## Stock

Create stock chart from Dataframe

If you use yahoo driverdrivers  you can pass it without option it's made to work together

Give a data frame with theses columns

| Date | Open | High | Low | Close | Adj Close | Volume | Company |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 2014-04-14 | 133.95 | 145.95 | 133.95 | 143.95 | 114.599 | 13650000 | TSLA |

You can give Moving average with column start with MA \(Max 2\)

| MA5 | MA20 |
| :--- | :--- |


You can plot prediction coming from prediction driver with theses column

| ARIMA | SVR | LINEAR | COMPOUND |
| :--- | :--- | :--- | :--- |
|  |  |  |  |

{% page-ref page="prediction.md" %}

all this data can be generated for you by the Yahoo driver

{% page-ref page="yahoo.md" %}

### Basic

```python
df = naas_drivers.yahoofinance.get("TSLA")
chart = naas_drivers.plotly.stock(df)
chart
```

### Chart type

```python
kind = "linechart" 
# can be linechart, linechart_open, linechart_close or candlestick
naas_drivers.plotly.stock("TSLA", kind=kind)
```

### Filter

```python
naas_drivers.plotly.stock("TSLA", filter=True, filter_title="Stock")
```

## Linechart

If you use yahoo driver you can pass it without option it's made to work together

### Basic

```python
df = naas_drivers.yahoofinance.get("TSLA")
chart = naas_drivers.plotly.linechart(df, label_x="Date", label_y=["Close"])
```

## Candlestick

If you use yahoo driver you can pass it without option it's made to work together

### Basic

```python
df = naas_drivers.yahoofinance.get("TSLA")
chart = naas_drivers.plotly.candlestick(df, 
                label_x="Date", 
                label_open="Open", 
                label_high="High",
                label_low="Low",
                label_close="Close"
                )
```

## Export

`SCREENSHOT_API`: this should be set as env vars. in local naas

this should connect to this docker machine :

{% embed url="https://hub.docker.com/r/anthonylau/url-to-pdf-api" %}

### Simple

```python
chart = naas_drivers.plotly.stock("TSLA")
filename = "Tesla.png" # can be png, jpeg or html
naas_drivers.plotly.export(chart, "Tesla.png", css=None)
```

### Css custom

```python
chart = naas_drivers.plotly.stock("TSLA")
filename = "Tesla.png" # can be png or html
css = ".custom_css {color: white}"
naas_drivers.plotly.export(chart, "Tesla.png", css=css)
```

## Official documentation:

{% embed url="https://plotly.com/python/getting-started/" %}

