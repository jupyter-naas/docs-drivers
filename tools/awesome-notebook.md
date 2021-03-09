---
description: Interact with our awesome notebook repo
---

# Awesome notebook

{% embed url="https://github.com/jupyter-naas/awesome-notebooks" %}



## Get list

```python
from naas_drivers import awesomeNotebooks, markdown

md_generated_list = awesomeNotebooks.connect().get()
markdown.display(md_generated_list)
```

## Create badge

```python
from naas_drivers import awesomeNotebooks

file_url = "https://github.com/jupyter-naas/awesome-notebooks/blob/master/Airtable/Airtable_connect.ipynb"
html_button = awesomeNotebooks.connect().badge(file_url)
html_button
```

