---
description: Create pdf from url
---

# 📄Pdf

## Connect

```python
import naas_drivers
naas_drivers.pdf.connect()
```

## Get

```text
url = "https://google.com"
filename = "google.pdf"
naas_drivers.pdf.get(url=url, filename=filename)
```

## Get from Html

```text
html = '<a src="https://google.com">test</a>'
filename = "google.pdf"
naas_drivers.pdf.get(html=html, filename=filename)
```

