---
description: Interact with Bubble app
---

# 🛁Bubble

### More details on official documentation:

{% embed url="https://bubble.io/reference\#API.swagger\_spec" %}

## Workflow

You can trigger workflow in bubble 

```python
import nass_drivers
url = "https://appname.bubbleapps.io/api/1.1/wf/endpoint_name"
data = { "first_name":"Bryan", "last_name":"Helmig", "age": 27 }
result = nass_drivers.zappier.run_workflow(url, data)
```

