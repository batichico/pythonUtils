
# Transform dict of dicts to list of dicts without key 
```
dict_t = {
    "key1": {
        "id": "key1",
        "message": "hi 1",
        "time": 1544123048630
    },
    "key2": {
        "id": "key2",
        "message": "hi 2",
        "time": 1544123055429
    }
}
contain = dict_t.values()
contain = [*contain]
print(contain)
```
Result:
```
[
  {
    'id': 'key1', 
    'message': 'hi 1', 
    'time': 1544123048630
   }, 
   {
    'id': 'key2', 
    'message': 'hi 2', 
    'time': 1544123055429
   }
]
```
