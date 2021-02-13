# Slack

How to get your bot token

Create app with the link below

{% embed url="https://api.slack.com/apps" %}

Then go to OAuth & Permissions

![Screenshot slack](../.gitbook/assets/screenshot-2021-01-25-at-18.24.42%20%281%29.png)

Add scope to your app to allow bot to speak ****[**chat:write.public**](https://api.slack.com/scopes/chat:write.public)\*\*\*\*

![Screenshot rights](../.gitbook/assets/screenshot-2021-01-25-at-18.24.33.png)

Then you sould reload your app, slack should notify you like this

![](../.gitbook/assets/screenshot-2021-01-25-at-19.54.48.png)

![Screenshot token](../.gitbook/assets/screenshot-2021-01-25-at-19.58.42.png)

Copy the Bot user OAuth Access Token and use it in the connect below

## Send message

```python
import naas_drivers

token = "xoxb-***-***-****"
message = "Hello friends"
result = naas_drivers.slack.connect(token).send(message)
```

### Image

Image be url only, if you need expose asset before sending it

```python
import naas_drivers

token = "xoxb-***-***-****"
message = "Hello friends"
image = "http://i.imgur.com/c4jt321l.png")
result = naas_drivers.slack.connect(token).send(message, image=image)
```

