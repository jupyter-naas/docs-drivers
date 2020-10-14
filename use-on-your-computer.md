---
description: Install Naas drivers in your local Jupyter environment.
---

# 🖥️ Use on your computer

## Is your local env ready?

Open a new notebook and check if the require env is set :

```python
import os
print('Yes' if (os.getenv('NB_USER') and os.getenv('JUPYTERHUB_USER') and os.getenv('JUPYTERHUB_API_TOKEN')) else 'No')
print(os.getenv('NB_USER'), os.getenv('JUPYTERHUB_USER'), os.getenv('JUPYTERHUB_API_TOKEN'))
```

#### Env requirements

* `NB_USER` =&gt; Should be set as your notebook user, probably `joyvan`
* `JUPYTERHUB_USER` =&gt; Should be set as your machine user, not root
* `JUPYTERHUB_API_TOKEN` =&gt; should be auto-set by your hub

## Install

Naas is a python module, install it with:

```python
!pip install nass_drivers
```

{% hint style="warning" %}
You can test on your local computer only the Scheduler feature.
{% endhint %}

{% hint style="danger" %}
Full install needs Kubernetes and Docker. Let's talk.
{% endhint %}

