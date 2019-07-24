# Example to validate web link
```
def linkSecure(link):
  isSecure = False
  lstEndLink = ["com","net","es","gg","info","de","org"]
  lstLink = link.split('.') 
  startLink = lstLink[0]
  endLink = lstLink[2]
  endLink = endLink.split("/")
  endLink = endLink[0]
  startLinkLen = len(lstLink[0])

  if len(startLink) == 11 and startLink == "https://www" :
    isSecure = True
  elif len(startLink) == 3 and startLink == "www":
    isSecure == True
  elif len(startLink) == 8 and startLink == "https://":
    isSecure = True
  else:
    isSecure = False
  if isSecure == True:
    for eLink in lstEndLink:
      if eLink == endLink or eLink == endLink+"/":
        isSecure = True
        break
      else:
        isSecure = False
  if isSecure == True:
    print("This link is secure")
  else:
    print("This link isn't secure")

link = "https://www.github.com/batichico/regex-python"
linkSecure(link)
```
