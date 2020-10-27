---
description: Interact with Jupyter app
---

# 🪐Jupyter

## Connect

You should get your token here

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

### uptime

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

### Active

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

