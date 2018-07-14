### Lambda
Lambda can be called as "one line function". Essentially you run it once, in a single line.


```python
add = lambda x,y : x + y
print ('Addition result      : {}'.format(add(3,4)))

mult = lambda x,y : x * y
print('Multiplication result: {}'.format(mult(3,4)))
```

    Addition result      : 7
    Multiplication result: 12



```python
numbers = [1,2,34,7,9,4]
print('Numbers                          : {}'.format(numbers))

factor2 = [x for x in numbers if x % 2 == 0]
print('Values where x mod 2 equal to 0  : {}'.format(factor2))

names = ['BOB','John','peter','JaNE']
print('Names                            : {}'.format(names))


names = [x.title() for x in names]
print('Names with first letter uppercase: {}'.format(names))

names = [x.lower() for x in names]
print('Lowercase all names              : {}'.format(names))

names = [name for name in names if 'e' in name]
print('Names with "e"                   : {}'.format(names))

```

    Numbers                          : [1, 2, 34, 7, 9, 4]
    Values where x mod 2 equal to 0  : [2, 34, 4]
    Names                            : ['BOB', 'John', 'peter', 'JaNE']
    Names with first letter uppercase: ['Bob', 'John', 'Peter', 'Jane']
    Lowercase all names              : ['bob', 'john', 'peter', 'jane']
    Names with "e"                   : ['peter', 'jane']
    
