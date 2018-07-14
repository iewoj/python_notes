## Variable Manipulation


```python
print("'" + a + "' vs '" + a.strip() + "'")
print("'" + a.center(25) + "'")
```

    '    28 Jun   2018   ' vs '28 Jun   2018'
    '       28 Jun   2018     '



```python
# Formatting
a = 'A Cat WalkeD dOwn the street.'
print("Default Output: {}".format(a))
print("Upper Output: {}".format(a.upper()))
print("Lower Output: {}".format(a.lower()))
```

    Default Output: A Cat WalkeD dOwn the street.
    Upper Output: A CAT WALKED DOWN THE STREET.
    Lower Output: a cat walked down the street.



```python
# Replacing a specific word
a = a.replace('Cat', 'Dog')
print (a)
```

    A Dog WalkeD dOwn the street.



```python
# Splitting by delimiter
a = 'apple, boy, cat'
print(a)
print(a.split(', '))
```

    apple, boy, cat
    ['apple', 'boy', 'cat']



```python
# String in string check
'a' in 'apple'
```




    True
