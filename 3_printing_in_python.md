## Printing Methods
+ Note that using ',' to separate will add a space
+ Note the following formats:
 + %d - integer
 + %f - float
 + %s - string


```python
name = 'Ben'
age = 10
print("My name is " + name + ", my age is " + str(age))
print("My name is", name, ", my age is ", str(age))
print("My name is {}, my age is {}".format(name, age))
print("My name is %s, my age is %d" % (name,age))
```

    My name is Ben, my age is 10
    My name is Ben , my age is  10
    My name is Ben, my age is 10
    My name is Ben, my age is 10


## Printing Statements


```python
a,b = 2,3
print (a, b, a+b)
print (round (12.34))
```

    2 3 5
    12



```python
a = '''hi, my name is Ben'''
print(a)
```

    hi, my name is Ben



```python
a = """hi, my name is Ben"""
print(a)
```

    hi, my name is Ben



```python
a = '''how to spell 'apple' and "banana" in Japanese'''
print(a)
```

    how to spell 'apple' and "banana" in Japanese



```python
# Variable Properties
a = '    28 Jun   2018   '
print("Length: {}".format(len(a)))
print("Type:   {}".format(type(a)))
```

    Length: 20
    Type:   <class 'str'>
    
