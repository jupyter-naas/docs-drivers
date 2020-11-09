---
description: Interact with Airtable app
---

# 💨Airtable

{% embed url="https://airtable.com/" caption="Website" %}

`apikey` should be generated in your account :

{% embed url="https://airtable.com/account" %}

You should find it there:

![Screenshot of account API section](.gitbook/assets/screenshot-2020-11-02-at-13.34.30.png)

then go on the upper link and choose the workspace you wanna connect and on the Authentication section, you should see :

![Screenshot of official doc](.gitbook/assets/screenshot-2020-11-02-at-13.30.21.png)

`database_key` is the value between `v0/` and `/` 

`table_name` is the value after the last `/` 

## Get

```python
import nass_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
data = nass_drivers.airtable
        .connect(api_key, database_key, table_name)
        .get(view='MyView', maxRecords=20)
```

## Send

```python
import nass_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
data = nass_drivers.airtable
        .connect(api_key, database_key, table_name)
        .send({'Name': 'Brian'})
```

## Search

```python
import nass_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
data = nass_drivers.airtable
        .connect(api_key, database_key, table_name)
        .search('Name', 'Tom')
```

## Update

```python
import nass_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
data = nass_drivers.airtable
        .connect(api_key, database_key, table_name)
        .update_by_field('Name', 'Tom', {'Phone': '1234-4445'})
```

## Delete

```python
import nass_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
data = nass_drivers.airtable
        .connect(api_key, database_key, table_name)
        .delete_by_field('Name', 'Tom')
```

## Connect

{% hint style="warning" %}
You can also save your connection and don't repeat it for each method.
{% endhint %}

```python
import nass_drivers
api_key = "******"
database_key = "appuBFPzX94pEqXUJ"
table_name = "Opportunities"
airtable = nass_drivers.airtable.connect(api_key, database_key, table_name)
data = airtable.get(view='MyView', maxRecords=20)
```

## Official documentation

{% embed url="https://airtable.com/api" caption="Documentation" %}

