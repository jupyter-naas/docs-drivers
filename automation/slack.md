# Slack

How to get your bot token



## Send message

```python
import naas_drivers

token = "xoxb-***-***-****"
message = "Hello friends"
result = naas_drivers.slack.connect(webhook).send(message)
```

