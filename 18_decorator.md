### Decorators

Decorators dynamically alter the functionality of a function, method, or class without having to directly use subclasses or change the source code of the function being decorated.

In a sense, allows you to transparently "wrap" the existing function with additional functionality. For example, from https://www.oreilly.com/ideas/5-reasons-you-need-to-learn-to-write-python-decorators:

Imagine this: you have a set of functions, each returning a dictionary, which (among other fields) includes a field called "summary." The value of this summary must not be more than 80 characters long; if violated, that’s an error.

Also, read https://www.thecodeship.com/patterns/guide-to-python-function-decorators/

In the example below, the _run_ function is "wrapped" by the *log_file* function so that when any os commands are issued, the output is written to log.txt


```python
import os
def log_file (func):
'''
takes any OS commands and wites result int log file
'''

def wrapper(command):
    command = command + " >> log.txt "
    return any_function(command)
return wrapper
```


```python
@log_file
def run(command):
os.system(command)
```


```python
run('date /T')

with open('log.txt','r') as fh:
output = fh.readlines()

print(output)
```

```
['Fri 07/13/2018 \n']
```
