---
description: Interact with our awesome notebook repo
---

# Awesome notebook

{% embed url="https://github.com/jupyter-naas/awesome-notebooks" %}



Get List 

```python
from naas_drivers import awesomeNotebooks, markdown

md_generated_list = awesomeNotebooks.connect().get()
markdown.display(md_generated_list)
```

