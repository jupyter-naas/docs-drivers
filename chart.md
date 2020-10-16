# 📊Plot

## Stock

Create stock chart

### Basic

```python
naas_drivers.plot().stock("TSLA")
```

### Date

```python
date_from = -30 # Date can be number or date or today
date_to = "today"
naas_drivers.plot().stock("TSLA", date_from=date_from, date_to=date_to)
```

### Interval

```python
naas_drivers.plot().stock("TSLA", interval="1d")
```

### Chart type

```python
kind = "candlestick" # can be linechart or candlestick
naas_drivers.plot().stock("TSLA", kind=kind)
```

### Filter

```python
naas_drivers.plot().stock("TSLA", filter=True, filter_title="Stock")
```

## Export

`SCREENSHOT_API`: this should be set as env vars.

this should connect to this docker machine :

{% embed url="https://hub.docker.com/r/anthonylau/url-to-pdf-api" %}



### Simple

```python
chart = naas_drivers.plot().stock("TSLA")
filename = "Tesla.png" # can be png or html
naas_drivers.plot().export(chart, "Tesla.png", css=None)
```

### Css

```python
chart = naas_drivers.plot().stock("TSLA")
filename = "Tesla.png" # can be png or html
css = ".custom_css {color: white}"
naas_drivers.plot().export(chart, "Tesla.png", css=css)
```

