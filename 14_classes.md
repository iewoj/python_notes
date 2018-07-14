# Classes
+ As with any object oriented programming language, Python supports classes.
+ Class is a programming construct and can be thought of as a "blueprint":
 + It is used to create and contain objects
 + It does not occupy any memory space like function definitions do

+ In practice, the statements inside a class definition will usually be function definitions

## Class vs Objects?
While class is also an object, a class as mentioned above is a programming construct. An __object__ is an instance of a __class__.

For example, a class may be a car blueprint and an object would be cars themselves.




```python
# Double underscrore is predefined properties for an object
# __init__ is a constructor
```


```python
class car():
    def __init__ (self, color = 'nope'):
        self.color = color
        print ('A car created with the color: {}'.format(color))
    def get_details (self):
        print('This car is in the color: {}'.format(self.color))
```


```python
carl = car('red')
john = car('blue')
```

    A car created with the color: red
    A car created with the color: blue



```python
# To get details:
carl.get_details()
john.get_details()
```

    This car is in the color: red
    This car is in the color: blue
