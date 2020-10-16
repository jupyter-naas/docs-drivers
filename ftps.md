# 📂🔒Ftps

## Connect

```python
 user = "my user"
 passwd = "my passwd"
 naas_drivers.ftps(user, passwd)
```

## Get file

```python
path = "/path/to/file/in/ftp"
user = "my user"
passwd = "my passwd"
naas_drivers.ftps(user, passwd).get(path)
```

## Send file

```python
path = "/path/to/local/file"
dest_path = "/path/to/file/in/ftp"
user = "my user"
passwd = "my passwd"
naas_drivers.ftps(user, passwd).get(path, dest_path)
```

## List file

```python
user = "my user"
passwd = "my passwd"
naas_drivers.ftps(user, passwd).list_directory()
```

