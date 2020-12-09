---
description: Interact with integromat app
---

# Integromat

{% embed url="https://integromat.com" %}

## WebHook

```python
import nass_drivers
url = "https://hook.integromat.com/7edtlwmn8foer0r9i9ainjvsz3vxmwos"
data = { "first_name":"Bryan", "last_name":"Helmig", "age": 27 }
result = nass_drivers.integromat.send(url, data)
```

## Official documentation

{% embed url="https://support.integromat.com/hc/en-us/articles/360006249313-Webhooks" caption="Documentation" %}

