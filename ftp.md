---
description: Connect to your ftp server
---

# 📂Ftp

## Connect

```python
 user = "my user"
 passwd = "my passwd"
 ftp = naas_drivers.ftps_toucan(user, passwd)
```

## Connect Secure \(FTPS\)

```python
 user = "my user"
 passwd = "my passwd"
 ftp = naas_drivers.ftps_toucan(user, passwd, port=990, secure=True)
```

## Connect and force Prot \(FTPS Toucan toco\)

```python
 user = "my user"
 passwd = "my passwd"
 ftp = naas_drivers.ftps_toucan(user, passwd, secure=True, force_prot=True)
```

## Get file

```python
path = "/path/to/file/in/ftp"
user = "my user"
passwd = "my passwd"
naas_drivers.ftp(user, passwd).get(path)
```

## Send file

```python
path = "/path/to/local/file"
dest_path = "/path/to/file/in/ftp"
user = "my user"
passwd = "my passwd"
naas_drivers.ftp(user, passwd).get(path, dest_path)
```

## List file

```python
user = "my user"
passwd = "my passwd"
naas_drivers.ftp(user, passwd).list_directory()
```

