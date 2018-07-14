## Inheritance
+ Classes can inherit from other classes.
+ Inheritance from a superclass includes attributes, functions, behavior methods

Example below is from: https://www.python-course.eu/python3_inheritance.php

Explanation:
+ _Person_ class takes in first name and last name and has a function definition: Name that combines and returns the name
+ _Employee_ class inherits the Name function from _Person_ class AND takes in a staff number
 + This is so that the Employee class does not have to (re)define any other attributes or methods already in _Person_ class





```python
class Person:
    def __init__ (self, first, last):
        self.firstname = first
        self.lastname = last

    def Name(self):
        return self.firstname + " " + self.lastname


class Employee (Person):
    def __init__(self, first, last, staffnum):
        Person.__init__(self, first, last)
        self.staffnumber = staffnum

    def GetEmployee(self):
        return self.Name() + ", " + self.staffnumber
```


```python
x = Person("Marge", "Simpson")
y = Employee("Homer", "Simpson", "1007")

print(x.Name())
print(y.GetEmployee())
```

    Marge Simpson
    Homer Simpson, 1007


Note the **self.variable**

This is so that variables within the class can be used freely among its definitions (global).

Otherwise, it is "local" within the premise of each definition only.


```python
class bank_account():
    def __init__(self, name, balance = 0):
        self.name = name
        self.balance = balance

    def get_details(self):
        print("My name: {} and my balance: {}".format(self.name, self.balance))


ben = bank_account("JOHN", 5)
ben.get_details()
```

    My name: JOHN and my balance: 5



```python
class bank_account():
    def __init__(self, name, balance = 0):
        self.name = name
        # self.balance = balance

    def get_details(self):
        print("My name: {} and my balance: {}".format(self.name, self.balance))


print("Because self.balance wasn't defined, get_details was not able to reference it!\n")
ben = bank_account("JOHN", 5)
ben.get_details()
```

    Because self.balance wasn't defined, get_details was not able to reference it!




    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-30-fd09b05576b4> in <module>()
         10 print("Because self.balance wasn't defined, get_details was not able to reference it!\n")
         11 ben = bank_account("JOHN", 5)
    ---> 12 ben.get_details()


    <ipython-input-30-fd09b05576b4> in get_details(self)
          5
          6     def get_details(self):
    ----> 7         print("My name: {} and my balance: {}".format(self.name, self.balance))
          8
          9


    AttributeError: 'bank_account' object has no attribute 'balance'
