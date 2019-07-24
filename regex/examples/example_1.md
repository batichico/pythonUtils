```import re```


# 1 Example
## Convert string with list inside to list 
```
s = 'acBarringFactor=95, acBarringForSpecialAC=[false, false, false, false, false], acBarringTime=64'

l = re.split('\[([^<^>])\]',s)

print(l)
```
result: 
```
['acBarringFactor=95, acBarringForSpecialAC=[false, false, false, false, false], acBarringTime=64']
```


# 2 Example
## Change chars for another chars
```
message = "(hi) man <how are you>"

charBetweenToChange1 = '<' #here you can set all chars that you want to detect and change
charBetweenToChange2 = '>' #here you can set all chars that you want to detect and change
charBetweenWant1 = '<b>' #here you can set all chars that you want set instead of "charBetweenToChange"
charBetweenWant2 = '</b>' #here you can set all chars that you want set instead of "charBetweenToChange"

#Here, we set chars that we want identify in the code.
messageFirstPart = '\$TOCHANGE1$([^<^>]+)\$TOCHANGE2$'
messageFirstPart = messageFirstPart.replace("$TOCHANGE1$",charBetweenToChange1)
messageFirstPart = messageFirstPart.replace("$TOCHANGE2$",charBetweenToChange2)

#Here, we set chars that we want to change using replace.
messageSecondPart = '$TOCHANGE1$\g<1>$TOCHANGE2$'
messageSecondPart = messageSecondPart.replace("$TOCHANGE1$",charBetweenWant1)
messageSecondPart = messageSecondPart.replace("$TOCHANGE2$",charBetweenWant2)

#Here we do conversion of chars. 
# "(hi) man <how are you>" to "(hi) man <b>how are you</b>"
message  = re.sub(r''+messageFirstPart, messageSecondPart, message)

print(message)
```
result:
```
"(hi) man <b>how are you</b>"
```


# 3 Example
## All elements that end with size 8 
```
re.match((\d{8}$))
```
```
dfopadpjfadf 12345678
```
