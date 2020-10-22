---
description: Interact with Zappier app
---

# 🤖 Integromat

### More details on the documentation here:

{% embed url="https://support.integromat.com/hc/en-us/articles/360006249313-Webhooks" %}



## WebHook

```python
import nass_drivers
url = "https://zapier.com/hooks/catch/n/Lx2RH/"
data = { "first_name":"Bryan", "last_name":"Helmig", "age": 27 }
result = nass_drivers.integromat.webhook(url, data)
```

