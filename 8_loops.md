## Loop Examples


```python
for alphabet in 'boy cat':
    print(alphabet)
```

    b
    o
    y

    c
    a
    t



```python
for i in [1,2,3,4]:
    print(i)
```

    1
    2
    3
    4



```python
set_a = {5, 3, 2, 1}
count = 0

for ele in set_a:
    print('Element {} in set with the value {}.'.format(count, ele))
    count+=1
```

    Element 0 in set with the value 1.
    Element 1 in set with the value 2.
    Element 2 in set with the value 3.
    Element 3 in set with the value 5.



```python
dict_a  = { 'a': 'apple', 'c': 'cat', 'b': 'bat', '1': 'one'}
for key, value in dict_a.items():
    print('Key is {}, Value is {}'.format(key, value))
```

    Key is a, Value is apple
    Key is c, Value is cat
    Key is b, Value is bat
    Key is 1, Value is one



```python
import collections
od = collections.OrderedDict(sorted(dict_a.items()))    
for key, value in od.items():
    print('Key is {}, Value is {}'.format(key, value))
```

    Key is 1, Value is one
    Key is a, Value is apple
    Key is b, Value is bat
    Key is c, Value is cat
