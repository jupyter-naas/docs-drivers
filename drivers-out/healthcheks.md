---
description: Interact with Healthchecks app
---

# ⛑ Healthchecks

{% embed url="https://healthchecks.io/" caption="Website" %}

If you are in naas cloud it's already setup, otherwise

`HC_API` : this should be set as env vars.

this should connect to this docker machine :

{% embed url="https://hub.docker.com/r/galexrt/healthchecks/" %}

## Start

```python
key = "123456-123456-12455"
naas_drivers.healthcheck.connect(key).send("start")
```

## Done

```python
key = "123456-123456-12455"
naas_drivers.healthcheck.connect(key).send()
```

## fail

```python
key = "123456-123456-12455"
naas_drivers.healthcheck.connect(key).send("fail")
```

## Check url

```python
url = "https://google.com"
key = "123456-123456-12455"
naas_drivers.health_check.connect(key).check_up(url)
```

## Connect

{% hint style="warning" %}
You can also save your connection and don't repeat it for each method.
{% endhint %}

```python
key = "123456-123456-12455"
healthcheck = naas_drivers.healthcheck.connect(key)
healthcheck.send()
```

## Official documentation



{% embed url="https://healthchecks.io/docs" %}

