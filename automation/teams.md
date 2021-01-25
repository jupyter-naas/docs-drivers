---
description: Send message in teams
---

# Teams

Get your webhook url there:

{% embed url="https://teams.microsoft.com/l/app/203a1e2c-26cc-47ca-83ae-be98f960b6b2?source=store-copy-link" %}

## Send message

```python
import naas_drivers

webhook = "https://COMPANY.webhook.office.com/webhookb2/****/***"
message = "Hello friends"
result = naas_drivers.teams.connect(webhook).send(message)
```
