# Slack

How to get your bot token

Create app with the link below

{% embed url="https://api.slack.com/apps" %}

Then go to OAuth & Permissions

![Screenshot slack](../.gitbook/assets/screenshot-2021-01-25-at-18.24.42%20%281%29.png)

Add scope to your app to allow bot to speak ****[**chat:write.public**](https://api.slack.com/scopes/chat:write.public)\*\*\*\*

![Screenshot rights](../.gitbook/assets/screenshot-2021-01-25-at-18.24.33.png)

## Send message

```python
import naas_drivers

token = "xoxb-***-***-****"
message = "Hello friends"
result = naas_drivers.slack.connect(webhook).send(message)
```

