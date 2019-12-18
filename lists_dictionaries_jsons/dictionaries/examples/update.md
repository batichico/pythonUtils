
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

# 3.- Save app into new key to new dict:
```
lst_updated = {}
notifications = {
    "1": {
        'app': 'securization', 
        'member_id': 'sam'
    },
    "2": {
        'app': 'securization', 
        'member_id': 'ann'
    },
    "3": {
        'app': 'desarrollo', 
        'member_id': 'peter'
    }
}
for noti in notifications:
    noti_app = notifications[noti]['app']
    noti_member_id = notifications[noti]['member_id']

    if noti_app in lst_updated:
        print("@lst_updated['securization']")
        print(lst_updated['securization'])
        lst_updated[noti_app].append(noti_member_id)

    else:
        lst_updated[noti_app] = [noti_member_id]

print()
print("lst_updated")
print(lst_updated)
```
