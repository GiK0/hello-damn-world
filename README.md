# hello-damn-world
first one
from urllib.request import urlopen

u = urlopen("")
word = {}
for line in u:
    line = line.strip(" \n")
    for word in line.split(" "):
        try:
            words[word] += 1
        except KeyError:
            words[word] = 1
pairs = words.items()
pairs.sort(key= lambda x: x[1], reverse = True)
for p in pairs[:40]:
    print (p[0], p[1])


    
