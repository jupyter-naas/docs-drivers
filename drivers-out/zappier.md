---
description: Interact with Zappier app
---

# ⚡️Zappier

### More details on the documentation here:

{% embed url="https://zapier.com/help/doc/how-get-started-webhooks-zapier" %}

## WebHook

```python
import nass_drivers
url = "https://zapier.com/hooks/catch/n/Lx2RH/"
data = { "first_name":"Bryan", "last_name":"Helmig", "age": 27 }
result = nass_drivers.zappier.webhook(url, data)
```

