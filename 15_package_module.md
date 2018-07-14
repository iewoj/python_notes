## Using module from packages
+ In addition to using the default modules from Python, you can write your own.
+ The example below shows user_functions package with two modules: *greetings* and *basic_add*

### From user_functions:
+ Copy the code below and save in the same directory as "user_functions.py"

```
def greetings (name = 'none'):
    print('Hello {}'.format(name))

def basic_add (x = 0, y = 0):
    result = x + y
    print('Result of addition: {}'.format(result))
```



```python
import user_functions as uf

uf.greetings('Peter')
uf.basic_add(2,3)
```

    Hello Peter
    Result of addition: 5



```python
from user_functions import greetings, basic_add

greetings('Spock')
basic_add(2,3)
```

    Hello Spock
    Result of addition: 5
