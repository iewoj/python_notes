## Regex

Functions:
+ match    - beginning of string
+ search   - everywhere within the string, one time
+ findall  - everywhere within the string, all
+ finditer - everywhere within the string, all iterators


```python
import re
```


```python
# MATCH
pat = re.compile(r'\d+')
m = pat.match('26 Jan 1999 is my birthday')

m.group()
```




    '26'




```python
# SEARCH
pat = re.compile(r'\d+')
m = pat.search('26 Jan 1999 is my birthday')

m.group()
```




    '26'




```python
# FINDALL
pat = re.compile(r'\d+')
m = pat.findall('26 Jan 1999 is my birthday')

for each in m:
    print(each)
```

    26
    1999
