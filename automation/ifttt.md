---
description: Interact with IFTTT.com
---

# IFTTT

{% embed url="https://ifttt.com" caption="Website" %}

Hit the documentation button to get your key :

![](../.gitbook/assets/screenshot-2020-10-19-at-15.17.36.png)

## WebHook

```python
import naas_drivers
event = "myevent"
key = "cl9U-VaeBu1**********"
data = { "value1": "Bryan", "value2": "Helmig", "value3": 27 }
result = naas_drivers.ifttt.connect(key).send(event, data)
```

## Official documentation

{% embed url="https://ifttt.com/maker\_webhooks/" caption="Documentation" %}

