## Replace the name of the greeting text with any name by parameter:

```
def replace_text(name):
    greet = "Hi [name], how are you?"
    greet_result = greet.replace("[name]", name)
    return greet_result

personalized_greet = replace_text("Peter") # Here we put the name of the person that you want to greet
print(personalized_greet)
```
result:
```
Hi Peter, how are you?
```
