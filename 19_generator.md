## Generator
Any function containing a yield keyword is a generator function; this is detected by Python’s bytecode compiler which compiles the function specially as a result.

When you call a generator function, it doesn’t return a single value; instead it returns a generator object that supports the iterator protocol. On executing the yield expression, the generator outputs the value of i, similar to a return statement. The big difference between yield and a return statement is that on reaching a yield the generator’s state of execution is suspended and local variables are preserved. On the next call to the generator’s __next__() method, the function will resume executing.

### Why?
+ Memory, think about infinite values
+ Observe no break in while loop


```python
def simple_generator(number):
    while True:
        yield number
        number = number + 1

```


```python
c = simple_generator(3)
next(c)
```




    3




```python
next(c)
```




    4




```python
next(c)
```




    5




```python
def my_gen():
    n = 1
    print('This is printed first')
    # Generator function contains yield statements
    yield n

    n += 1
    print('This is printed second')
    yield n

    n += 1
    print('This is printed at last')
    yield n
```


```python
a = my_gen()
next(a)
```

    This is printed first





    1




```python
next(a)
```

    This is printed second





    2




```python
next(a)
```

    This is printed at last





    3




```python
next(a)
```


    ---------------------------------------------------------------------------

    StopIteration                             Traceback (most recent call last)

    <ipython-input-75-15841f3f11d4> in <module>()
    ----> 1 next(a)


    StopIteration:
