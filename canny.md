---
description: Interact with canny app
---

# 🥫Canny

{% embed url="https://developers.canny.io/api-reference" %}

## Users

### Get

```python
import nass_drivers
api_key = "api_key"
naas_drivers.canny.connect(api_key).users.get(
    uid="uid"
)
```

### Send

```python
import nass_drivers
api_key = "api_key"
naas_drivers.canny.connect(api_key).send(
    email="bob@cashstory.com"
)
```

### Get by email

```python
import nass_drivers
api_key = "api_key"
naas_drivers.canny.connect(api_key).users.get_by_email(
    email="bob@cashstory.com"
)
```

### Delete

```python
import nass_drivers
api_key = "api_key"
naas_drivers.canny.connect(api_key).users.delete(
    uid="uid"
)
```

## Connect

{% hint style="warning" %}
You can also save your connection and don't repeat it for each method.
{% endhint %}

```python
import nass_drivers
api_key = "api_key"
canny = nass_drivers.canny.connect(api_key)
data = canny.users.get()
```

## Official documentation

{% embed url="https://canny.io/" %}





