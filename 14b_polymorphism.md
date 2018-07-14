## Polymorphism

+ The idea here is to use the same "interface" to address different forms of objects or data types.
+ Polymorphism is an important feature of class definition in Python that is utilized when you have commonly named methods across classes or subclasses. This allows functions to use objects of any of these polymorphic classes without needing to be aware of distinctions across the classes.
+ Based on the class, it can return different definitions with the same "interface"



```python
class fish():
    def nature (self):
        print('I can swim!')

class bird():
    def nature (self):
        print('I can fly!')

class monkey():
    def nature (self):
        print('I can climb!')

```


```python
salmon = fish()
hawk   = bird()
chimp  = monkey()

salmon.nature()
hawk.nature()
chimp.nature()
```

    I can swim!
    I can fly!
    I can climb!
