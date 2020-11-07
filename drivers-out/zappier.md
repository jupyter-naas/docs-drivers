---
description: Interact with Zapier app
---

# ⚡️Zapier

{% embed url="http://zappier.com/" caption="Website" %}

## WebHook

```python
import naas_drivers
url = "https://zapier.com/hooks/catch/n/Lx2RH/"
data = { "first_name":"Bryan", "last_name":"Helmig", "age": 27 }
result = nass_drivers.zappier.send(url, data)
```

## Official documentation

{% embed url="https://zapier.com/help/doc/how-get-started-webhooks-zapier" caption="Documentation" %}

