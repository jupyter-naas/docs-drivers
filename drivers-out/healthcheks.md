---
description: Interact with Healthcheks app
---

# ⛑Healthcheks

{% embed url="https://healthchecks.io/" caption="Website" %}

If you are in naas cloud it's already setup, otherwise

`HC_API` : this should be set as env vars.

this should connect to this docker machine :

{% embed url="https://hub.docker.com/r/galexrt/healthchecks/" %}

## Start

```python
key = "123456-123456-12455"
naas_drivers.healthcheck.send(key, "start")
```

## Done

```python
key = "123456-123456-12455"
naas_drivers.healthcheck.send(key)
```

## fail

```python
key = "123456-123456-12455"
naas_drivers.healthcheck.send(key, "fail")
```

## Check url

```python
url = "https://google.com"
key = "123456-123456-12455"
naas_drivers.health_check.check_up(url, key)
```

## Official documentation

{% embed url="https://healthchecks.io/docs" %}

