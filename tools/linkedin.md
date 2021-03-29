---
description: Improve your KYC thanks to Linkedin connection
---

# Linkedin

{% embed url="https://www.linkedin.com" %}

## Connect

{% hint style="info" %}
To "connect", inspect your linkedin page while connected and get your cookies info in "Application" tab :

* li\_at
* JSESSIONID
{% endhint %}

## Get 

### Linkedin profil

```python
from naas_drivers import linkedin

LI_AT = 'YOUR_COOKIE_LI_AT'  # EXAMPLE AQFAzQN_PLPR4wAAAXc-FCKmgiMit5FLdY1af3-2
JSESSIONID = 'YOUR_COOKIE_JSESSIONID'  # EXAMPLE ajax:8379907400220387585
linkedinid = "LINKEDIN_PROFILE"

profil = linkedin.connect(LI_AT, JSESSIONID).get_profil(linkedinid)
profil
```

### Last 20 messages

```python
from naas_drivers import linkedin

LI_AT = 'YOUR_COOKIE_LI_AT'  # EXAMPLE AQFAzQN_PLPR4wAAAXc-FCKmgiMit5FLdY1af3-2
JSESSIONID = 'YOUR_COOKIE_JSESSIONID'  # EXAMPLE ajax:8379907400220387585

df_messages = linkedin.connect(LI_AT, JSESSIONID).get_messages()
df_messages
```

## Advanced

{% hint style="warning" %}
You can "Connect" before any other methods and use your object in your formulas
{% endhint %}

```python
from naas_drivers import linkedin

LI_AT = 'YOUR_COOKIE_LI_AT'  # EXAMPLE AQFAzQN_PLPR4wAAAXc-FCKmgiMit5FLdY1af3-2
JSESSIONID = 'YOUR_COOKIE_JSESSIONID'  # EXAMPLE ajax:8379907400220387585

# Connect to Linkedin
LK = linkedin.connect(LI_AT, JSESSIONID)

# Get last 20 messages
df_messages = LK.get_messages()
```

