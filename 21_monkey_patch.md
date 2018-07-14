## Monkey patch - mask functions

Here we overwrite the function definition of randint and 'redirect' it to monkeypatch, which will always return unavailable


```python
import random

random.randint(1, 10)
```




    2




```python
def monkey_patch (a, b):
    print('Random function temporarily unavailable')
    print('Sorry for the inconvenience')
    return a
```


```python
random.randint = monkey_patch
```


```python
random.randint(1, 19)
```

    Random function temporarily unavailable
    Sorry for the inconvenience





    1
