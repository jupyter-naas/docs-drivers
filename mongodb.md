---
description: Fetch data from a mongodb and get a dataframe
---

# 🥭MongoDb

## Connect

```python
 user = "my user"
 passwd = "my passwd"
 host = "url"
 port = 9090
 ftp = naas_drivers.mongo.connect(host, port, user, passwd)
```

## Get data

```python
collection_name = "col"
db_name = "db_name"
naas_drivers.mongo.get(collection_name, db_name)
```

## Send data

```python
collection_name = "col"
db_name = "db_name"
data = # a dataframe
naas_drivers.mongo.send(data, collection_name, db_name)
```
