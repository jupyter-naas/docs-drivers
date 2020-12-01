---
description: Interact with Airtable app
---

# 💨 Airtable

{% embed url="https://airtable.com/" caption="Website" %}

`apikey` should be generated in your account :

{% embed url="https://airtable.com/account" %}

You should find it there:

![Screenshot of account API section](.gitbook/assets/screenshot-2020-11-02-at-13.34.30.png)

Then go to :

{% embed url="https://airtable.com/api" %}

 and choose the workspace you wanna connect and on the Authentication section, you should see :

![Screenshot of official doc](.gitbook/assets/screenshot-2020-11-02-at-13.30.21.png)

`database_key` is the value between `v0/` and `/` 

`table_name` is the value after the last `/` 

## Get

```python
import naas_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
view = "MyView" # the name of your view in airtable
at = naas_drivers.airtable.connect(api_key, database_key, table_name)
data = at.get(view=view, maxRecords=20)
```

## Send

```python
import naas_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
at = naas_drivers.airtable.connect(api_key, database_key, table_name)
data = at.send({'Name': 'Brian'})
```

## Search

```python
import naas_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
at = naas_drivers.airtable.connect(api_key, database_key, table_name)
data = at.search('Name', 'Tom')
```

## Update

```python
import naas_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
at = naas_drivers.airtable.connect(api_key, database_key, table_name)
data = at.update_by_field('Name', 'Tom', {'Phone': '1234-4445'})
```

## Delete

```python
import naas_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
at = naas_drivers.airtable.connect(api_key, database_key, table_name)
data = at.delete_by_field('Name', 'Tom')
```

## Connect

{% hint style="warning" %}
You can also save your connection and don't repeat it for each method.
{% endhint %}

```python
import naas_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
at = naas_drivers.airtable.connect(api_key, database_key, table_name)
data = at.get(view='MyView', maxRecords=20)
```

## Official documentation

{% embed url="https://airtable.com/api" caption="Documentation" %}

