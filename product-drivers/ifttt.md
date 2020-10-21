---
description: Interact with Zappier app
---

# ➕IFTTT

### More details on the documentation here:

{% embed url="https://ifttt.com/maker\_webhooks/" %}

Hit the documentation button to get your key :

![](../.gitbook/assets/screenshot-2020-10-19-at-15.17.36.png)

## WebHook

```python
import naas_drivers
event = "myevent"
key = "cl9U-VaeBu1**********"
data = { "value1": "Bryan", "value2": "Helmig", "value3": 27 }
result = nass_drivers.ifttt().webhook(event, key, data)
```



