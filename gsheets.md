---
description: Fetch data from a sheet in google spreadsheet and get a dataframe
---

# 📈Gsheets

{% embed url="https://www.google.com/sheets/about/" %}

## Share your google sheet with service account

For the driver to fetch the contents of your google sheet, you need to share it with the service account linked with **naas**.

{% hint style="info" %}
 Share your sheet with `naas-share@naas-gsheets.iam.gserviceaccount.com`
{% endhint %}

Now you can fetch data from the sheet as a pandas dataframe.

## Get

```python
import nass_drivers
spreadsheet_id = "idd"
naas_drivers.gsheet.connect(spreadsheet_id).get(
    sheet_name="name"
)
```

## Send

```python
data = [{ "name": "Jean", "email": "jean@appleseed.com" }, { "name": "Bunny", "email": "bunny@appleseed.com" }]
spreadsheet_id = "idd"
naas_drivers.gsheet.connect(spreadsheet_id).send(
    sheet_name="TSLA",
    data
)
```

## Connect

{% hint style="warning" %}
You can also save your connection and don't repeat it for each method.
{% endhint %}

```python
gsheet = naas_drivers.gsheet.connect("spreadsheet_id")

name_1 = cityfalcon.get("name_1")
name_2 = cityfalcon.get("name_2")
```

## Official documentation

{% embed url="https://github.com/melalj/gsheet-api" %}

