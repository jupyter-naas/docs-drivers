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

## Get data

```python
naas_drivers.gsheet.get(
    spreadsheet_id="sadf3q123413asffd123",
    sheet_name="TSLA"
)
```

## Send data

```python
naas_drivers.gsheet.send(
    spreadsheet_id="sadf3q123413asffd123",
    sheet_name="TSLA",
    data
)
```



