---
description: Connect to news api
---

# 🆕 News api

### More details on official documentation:

{% embed url="https://newsapi.org/docs/endpoints" %}

## Connect

```python
naas_drivers.newsapi.connect("API_KEY")
```

## Get

### Action

```python
naas_drivers.newsapi.get("TSLA")
```

### Fields

Choose fields you want to get in result, list available below:

* title
* image
* link
* description
* source
* image

```python
fields = ["image", "title"]
naas_drivers.newsapi.get("TSLA", fields=fields)
```

### Language

Language of news

```python
country = "en"
data = naas_drivers.newsapi.get("TSLA", language=country)
```

### Limit

Limit the number of result 

```python
limit = 5
data = naas_drivers.newsapi.get("TSLA", limit=limit)
```

## Get top news

```python
data = naas_drivers.newsapi.get_top(sources='bbc-news')
```

## Get sources news

```python
sources = naas_drivers.newsapi.get_sources()
```

