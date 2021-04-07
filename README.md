# configGen
gennerate config file from multy config files, print merged results.

# usage
a.conf:
```ini
username=Jack
age=20
```

b.conf:
```ini
username=Lucy
age=30
passwd=123
```

then
```shell
# ./confgen a.conf
```
outputs:
```ini
# Loading a.conf
username = Jack
age = 20
```

```shell
# ./confgen a.conf b.conf
```
outputs:
```ini
# Loading a.conf
# Loading b.conf
username = Lucy
age = 30
passwd = 123
```

The output = a.conf + b.conf. You can add as many config files as you want, at least one.

To satisfied with config files that common in Linux System, the first INI section is ignored, you may add it manually.



