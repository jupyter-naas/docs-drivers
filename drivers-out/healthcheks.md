---
description: Interact with Healthcheks app
---

# ⛑Healthcheks

{% embed url="https://healthchecks.io/" caption="Website" %}

If you are in naas cloud it's already setup, otherwise

`HC_API` : this should be set as env vars.

this should connect to this docker machine :

{% embed url="https://hub.docker.com/r/galexrt/healthchecks/" %}

## Connect

{% hint style="danger" %}
You must Connect before any other methods
{% endhint %}

```python
key = "123456-123456-12455"
naas_drivers.healthcheck.connect(key)
```

## Start

```python
naas_drivers.healthcheck.send("start")
```

## Done

```python
naas_drivers.healthcheck.send()
```

## fail

```python
naas_drivers.healthcheck.send("fail")
```

## Check url

```python
url = "https://google.com"
naas_drivers.health_check.check_up(url)
```

## Official documentation

{% embed url="https://healthchecks.io/docs" %}

