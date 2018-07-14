## Beautiful Code
This section is on how to write codes and document them more efficiently.


```python
names = ['raymond', 'rachle' ,'robin']
colors = ['red', 'green', 'blue','yellow']

n = min(len(names), len(colors))
```

Instead of creating a counter and looping it through the element, get the minimum length of the lists into a variable.


```python
for i in range(n):
    print(names[i], '-->', colors[i])
```

    raymond --> red
    rachle --> green
    robin --> blue


+ If no parameters are passed, zip() returns an empty iterator
+ If a single iterable is passed, zip() returns an iterator of 1-tuples. Meaning, the number of elements in each tuple is 1.
+ If multiple iterables are passed, ith tuple contains ith Suppose, two iterables are passed; one iterable containing 3 and other containing 5 elements. Then, the returned iterator has 3 tuples. It's because iterator stops when shortest iterable is exhaused.


```python
for name, color in zip (names, colors):
    print (name, '-->', color)
```

    raymond --> red
    rachle --> green
    robin --> blue
    
