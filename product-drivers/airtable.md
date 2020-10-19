---
description: Interact with Airtable app
---

# 💨Airtable

## Connect

```python
import nass_drivers
airtable = nass_drivers.airtable('baseKey', 'table_name')
```

## Get all

```python
import nass_drivers
airtable = nass_drivers.airtable('baseKey', 'table_name')

airtable.get_all(view='MyView', maxRecords=20)
```

## Insert

```python
import nass_drivers
airtable = nass_drivers.airtable('baseKey', 'table_name')

airtable.insert({'Name': 'Brian'})
```

## Search

```python
import nass_drivers
airtable = nass_drivers.airtable('baseKey', 'table_name')

airtable.search('Name', 'Tom')
```

## Update

```python
import nass_drivers
airtable = nass_drivers.airtable('baseKey', 'table_name')

airtable.update_by_field('Name', 'Tom', {'Phone': '1234-4445'})
```

## Delete

```python
import nass_drivers
airtable = nass_drivers.airtable('baseKey', 'table_name')

airtable.delete_by_field('Name', 'Tom')
```

