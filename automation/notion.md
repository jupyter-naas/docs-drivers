---
description: Interact with Notion app
---

# Notion

{% embed url="https://www.notion.so/login" caption="Login link" %}

Before start, you have to connect to your account in notion and get your session token

![](../.gitbook/assets/screenshot-2021-02-10-at-22.34.57.png)

Click right on the notion page and select inspect

![](../.gitbook/assets/screenshot-2021-02-10-at-22.39.29.png)

Then select the Application tab \( in the red box \)

![](../.gitbook/assets/screenshot-2021-02-10-at-22.35.34.png)

Select the cookies section and the notion url as show in the screenshot 

Then look for the `token_v2`and copie the value on the right , this is the way to login in your notion.

## Connect

{% hint style="danger" %}
You must "Connect" before any other methods
{% endhint %}

```python
from naas_drivers import notion

# Enter your Auth token
token = "*********"

# Connect to hubspot
hs = notion.connect(token=token)
```

## Get

```python
import naas_drivers

token = "*********"
url = "https://www.notion.so/myorg/Test-c0d20a71c0944985ae96e661ccc99821"
page = naas_drivers.notion.connect(token=token).get(url)

```

## Get collection

```python
import naas_drivers

token = "*********"
url = "https://www.notion.so/myorg/Test-c0d20a71c0944985ae96e661ccc99821"
collection_df = naas_drivers.notion.connect(token=token).get_collection(url)
```

You can also get it in raw format to be able to edit it :

```python
import naas_drivers

token = "*********"
url = "https://www.notion.so/myorg/Test-c0d20a71c0944985ae96e661ccc99821"
n = naas_drivers.notion.connect(token=token)
collection = n.get_collection(url, raw=True)
```

