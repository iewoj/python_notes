## Iterator
+ Consumes less memory space
+ Runs one at a time



```python
a = [1,2,3]
b = iter(a)
next(b)
```




    1




```python
next(b)
```




    2




```python
next(b)
```




    3




```python
next(b)
```


    ---------------------------------------------------------------------------

    StopIteration                             Traceback (most recent call last)

    <ipython-input-65-adb3e17b0219> in <module>()
    ----> 1 next(b)


    StopIteration:
