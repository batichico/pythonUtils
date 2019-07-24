
# 1.- Update({'key': value}) to add at the end of the dictionary one key with is value:
```
user = {
    'name': 'Patrick',
    'city': 'London',
    'phone': 123132
}
user.update({'age': 30})
print(user)
```
result:
```
{'name': 'Patrick', 'city': 'London', 'phone': 123132, 'age': 30}
```

# 2.- Update({'key': value}) to update setted key value:
```
user = {
    'name': 'Patrick',
    'city': 'London',
    'phone': 123132,
    'age': 3
}
user.update({'age': 30})
print(user)
```
result:
```
{'name': 'Patrick', 'city': 'London', 'phone': 123132, 'age': 30}
```
