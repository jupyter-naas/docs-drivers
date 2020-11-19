---
description: Interact with Jupyter app
---

# 🪐 Jupyter

{% embed url="https://jupyter.org/hub" caption="Website" %}

## Connect

{% hint style="danger" %}
You must Connect before any other methods
{% endhint %}

You should get your token here :

{% hint style="success" %}
In Naas cloud you can connect without any argument it will find your token alone
{% endhint %}

{% embed url="https://app.naas.ai/hub/token" %}

```text
token = "*****"
jp = naas_drivers.jupyter.connect(token)
```

## Me

### Get 

```text
me = jp.get_me()
```

### Uptime

```text
uptime = jp.get_me_uptime()
```

## Admin

Only Naas admin can do it

### Users

```text
users = jp.get_users()
```

### User

```text
email = "bob@cashstory.com"
user = jp.get_user(email)
```

### Create

```text
email = "bob@cashstory.com"
password = "****"
user = jp.create_user(email, password)
```

### Get Authorize

Get one Authorization for user.

```text
email = "bob@cashstory.com"
is_authorize = jp.get_authorize_user(email)
```

### Authorize

Authorize one user.

```text
email = "bob@cashstory.com"
is_authorize = True
user = jp.change_authorize_user(email, is_authorize)
```

### Active

check if user has running server

```text
active = jp.is_user_active(user)
```

### Server uptime

```text
uptime = jp.get_server_uptime(user)
```

### Stop user

```text
jp.stop_user(user)
```

### Start user

```text
jp.start_user(user)
```

### Restart user

```text
jp.restart_user(user)
```

## Official documentation

{% embed url="https://jupyterhub.readthedocs.io/en/stable/reference/rest.html" %}

