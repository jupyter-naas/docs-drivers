---
description: Interact with email box
---

# 💌 Email

## Connect

{% hint style="warning" %}
You can save your connection and don't repeat it for each method.
{% endhint %}

```python
username = "USERNAME"
password = "PASSWORD"
email_from = "bob@cashstory.com",
smtp_server = "smtp.sendgrid.net",
smtp_port = 465,
smtp_type = "SSL",

emails = nass_drivers.email.connect(username, 
        password, 
        email_from, 
        smtp_server, 
        smtp_port,
        smtp_type)
```

## Text

Send an email to anyone, notify about data changes, alert on notebooks operations, etc... 

```python
email = "elon@musk.com"
subject = "The tesla action is going up"
content = "check in the link the chart data maide from fresh dataset : [LINK]"

emails.send(email_to=email, subject=subject, html=content)
```

## File

```python
email = "elon@musk.com"
subject = "The tesla action is going up"
content = "check in the link the chart data maide from fresh dataset : [LINK]"'
files = ["path/to/my/super/data.csv"]

emails.send(email_to=email, subject=subject, html=content, files=files)
```

## HTML

```python
email = "elon@musk.com"
subject = "The tesla action is going up"
image_path = "path/to/my/super/data.png"
html = f"<h1>Check in the link the chart image below</h1><br/> <img src="{image_path}"/>"

emails.send(email_to=email, subject=subject, html=content)
```



## 

