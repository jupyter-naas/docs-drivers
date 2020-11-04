---
description: Connect to cityfalcon api and get a dataframe
---

# 📰Cityfalcon

{% embed url="https://www.cityfalcon.com/" caption="Website" %}

## Connect

```python
naas_drivers.cityfalcon.connect("YOUR_API_KEY")
# You can use our default apikey limited to 200/hours request for all users 
naas_drivers.cityfalcon.connect()
```

## Get

### Action

```python
naas_drivers.cityfalcon.get("TSLA")
```

### Fields

Choose fields you want to get in result, list available below:

* title
* image
* link
* description
* score
* sentiment
* source
* source\_logo
* image

```python
fields = ["image", "title"]
naas_drivers.cityfalcon.get("TSLA", fields=fields)
```

### Country

Country of stock exange

```python
country = "US"
naas_drivers.cityfalcon.get("TSLA", country=country)
```

### Limit

Limit the number of result 

```python
limit = 5
naas_drivers.cityfalcon.get("TSLA", limit=limit)
```

### Minimum Score

minimum Score of Cityfalcon 

```python
min_score = 30
naas_drivers.cityfalcon.get("TSLA", min_score=min_score)
```

### Paywall

Show article with paywall

```python
paywall = True
naas_drivers.cityfalcon.get("TSLA", paywall=paywall)
```

### Identifier\_type

```python
identifier_type = "full_tickers"
naas_drivers.cityfalcon.get("TSLA", identifier_type=identifier_type)
```

### Time\_filter

```python
time_filter = "d21"
naas_drivers.cityfalcon.get("TSLA", time_filter=time_filter)
```

### Language

```python
naas_drivers.cityfalcon.get("TSLA", languages="en")
```

## Official documentation

{% embed url="https://dev.cityfalcon.com/doc/api/v0.2" %}

