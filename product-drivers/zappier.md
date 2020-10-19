---
description: Interact with Zappier app
---

# ⚡️Zappier

## WebHook

```python
import nass_drivers
url = "https://zapier.com/hooks/catch/n/Lx2RH/"
send = { "first_name":"Bryan", "last_name":"Helmig", "age": 27 }
result = nass_drivers.zappier.webhook(url, send)
```

