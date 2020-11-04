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

## Connect

{% hint style="danger" %}
You must Connect before any other methods
{% endhint %}

```python
import nass_drivers
spreadsheet_id = "idd"
airtable = nass_drivers.gsheet.connect(spreadsheet_id)
```

## Get data

```python
naas_drivers.gsheet.get(
    sheet_name="TSLA"
)
```

## Send data

```python
data = [{ "name": "Jean", "email": "jean@appleseed.com" }, { "name": "Bunny", "email": "bunny@appleseed.com" }]
naas_drivers.gsheet.send(
    sheet_name="TSLA",
    data
)
```

## Official documentation

{% embed url="https://github.com/melalj/gsheet-api" %}

