---
description: Fetch data from a sheet in google spreadsheet.
---

# Gsheets

## Share your google sheet with service account

For the driver to fetch the contents of your google sheet, you need to share it with the service account linked with **naas**.

{% hint style="info" %}
 Share your sheet with `naas-share@naas-gsheets.iam.gserviceaccount.com`
{% endhint %}

Now you can fetch data from the sheet as a pandas dataframe.

```python
naas_drivers.gsheet(
    spreadsheet_id="sadf3q123413asffd123",
    sheet_id="TSLA"
)
```



