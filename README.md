# WordList

custom fuzzing wordlist
```
cat urls.txt | sed 's|\(.*\)/[^/]*$|\1|' | cut -d"/" -f4,5,6,7,8,9,10,11 | tr "/" "\n" | sed '/^$/d' | anew fuzzing_list.txt
```

custom dns wordlist
```
cat alltargets.txt | sed 's/\.[^.]*$//' | tr "." "\n" | egrep -v '^[0-9]*$' | anew dns-wordlist.txt
```

custom urls for nuclei automation
```
cat urls.txt | sed 's|\(.*\)/[^/]*$|\1|' | cut -d'/' -f1-6 | anew urls.txt
cat urls.txt | sed 's|\(.*\)/[^/]*$|\1|' | cut -d'/' -f1-5 | anew urls.txt
cat urls.txt | sed 's|\(.*\)/[^/]*$|\1|' | cut -d'/' -f1-4 | anew urls.txt
```
