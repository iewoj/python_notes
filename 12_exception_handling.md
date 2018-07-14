## Exception Handling


```python
def divide(x,y):
    try:
        value = x / y
        print('PASS: Value = {}'.format(value))
    except:
        print('ERROR: Division by zero')
    finally:
        print('This line is always executed at the end of a try statement')
```


```python
divide(4, 2)
```

    PASS: Value = 2.0
    This line is always executed at the end of a try statement



```python
divide(2, 0)
```

    ERROR: Division by zero
    This line is always executed at the end of a try statement


### Assertion


```python
a = float(input("current temperature: "))
```

    current temperature: 50



```python
assert a > 17 and a < 45, 'Current temperature is NOT between 17 and 45'
```


    ---------------------------------------------------------------------------

    AssertionError                            Traceback (most recent call last)

    <ipython-input-171-57ca956f4775> in <module>()
    ----> 1 assert a > 17 and a < 45, 'Current temperature is NOT between 17 and 45'


    AssertionError: Current temperature is NOT between 17 and 45



```python
a = input('Enter pin number: ')
if len(a) < 4:
    raise AttributeError
else:
    print('Pin number length: {}'.format(len(a)))
```

    Enter pin number: 123456
    Pin number length: 6



```python
a = input('Enter pin number: ')
if len(a) < 4:
    raise AttributeError
else:
    print('Pin number length: {}'.format(len(a)))
```

    Enter pin number: 123



    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-182-47bfbd08d670> in <module>()
          1 a = input('Enter pin number: ')
          2 if len(a) < 4:
    ----> 3     raise AttributeError
          4 else:
          5     print('Pin number length: {}'.format(len(a)))


    AttributeError:
