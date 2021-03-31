---
description: Interact with our awesome notebook repo
---

# Awesome notebook

{% embed url="https://github.com/jupyter-naas/awesome-notebooks" %}



## Get list

```python
import naas_drivers

naas_drivers.templates.get()
```

## Create badge

```python
import naas_drivers

file_url = "https://github.com/jupyter-naas/awesome-notebooks/blob/master/Airtable/Airtable_connect.ipynb"
naas_drivers.templates.badge(file_url)
```

