
# Introduction to Python
 + An interpreted high-level programming language for general-purpose programming
 + Created by Guido van Rossum and first released in 1991
  + Python has a design philosophy that emphasizes code readability, notably using significant whitespace
 + Python is scalable and offers flexibility allowing one to write a code for something as simple as file-based processing to data analysis leveraging on modules such as pandas and numpy.


## A few basic notes...
For those with some background in other programming languages, here's the lowdown for Python:
+ Be **CONSISTENT**:
 + It is space and tab sensitive - mixing spaces and tabs are not allowed
 + Using a single quote (') or double quotes (") makes no difference
+ Python 3 requires any print statement to be in brackets while it is optional in previous versions

## Primitive Data Structures
+ Python has the usual set of basic variable types such as:
 + Integer
 + Float
 + String
 + Boolean
 
### Defining Variables


```python
# INTEGER
a = 1
print("Value: {}, and Type: {}".format(a, type(a)))
```

    Value: 1, and Type: <class 'int'>
    


```python
# FLOAT
a = 10.5
print("Value: {}, and Type: {}".format(a, type(a)))
```

    Value: 10.5, and Type: <class 'float'>
    


```python
# STRING
a = "foo"
print("Value: {}, and Type: {}".format(a, type(a)))
```

    Value: foo, and Type: <class 'str'>
    


```python
# BOOLEAN
a = True
print("Value: {}, and Type: {}".format(a, type(a)))
```

    Value: True, and Type: <class 'bool'>
    

## Variable Manipulation


```python
print("'" + a + "' vs '" + a.strip() + "'")
print("'" + a.center(25) + "'")
```

    '    28 Jun   2018   ' vs '28 Jun   2018'
    '       28 Jun   2018     '
    


```python
# Formatting
a = 'A Cat WalkeD dOwn the street.'
print("Default Output: {}".format(a))
print("Upper Output: {}".format(a.upper()))
print("Lower Output: {}".format(a.lower()))
```

    Default Output: A Cat WalkeD dOwn the street.
    Upper Output: A CAT WALKED DOWN THE STREET.
    Lower Output: a cat walked down the street.
    


```python
# Replacing a specific word
a = a.replace('Cat', 'Dog')
print (a)
```

    A Dog WalkeD dOwn the street.
    


```python
# Splitting by delimiter
a = 'apple, boy, cat'
print(a)
print(a.split(', '))
```

    apple, boy, cat
    ['apple', 'boy', 'cat']
    


```python
# String in string check
'a' in 'apple'
```




    True



## Printing Methods


```python
name = 'Ben'
age = 10
print("My name is {}, my age is {}".format(name, age))
print("My name is %s, my age is %d" % (name,age))
print("My name is " + name + ", my age is " + str(age))
print("My name is", name, ", my age is ", str(age))
```

    My name is Ben, my age is 10
    My name is Ben, my age is 10
    My name is Ben, my age is 10
    My name is Ben , my age is  10
    

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
    

## Math Operation


```python
a = 2 * 3
print("Value: {}, and Type: {}".format(a, type(a)))
```

    Value: 6, and Type: <class 'int'>
    


```python
a = 2 ** 3
print("Value: {}, and Type: {}".format(a, type(a)))
```

    Value: 8, and Type: <class 'int'>
    


```python
a = 3 / 2.0
print("Value: {}, and Type: {}".format(a, type(a)))
```

    Value: 1.5, and Type: <class 'float'>
    

## Taking Keyboard Inputs


```python
a = input('Enter age: ')
print('Your age is: {}'.format(a.strip()))
```

    Enter age: 26
    Your age is: 26
    

## File Inputs


```python

```


```python

```

## Non-primitive Data Structures
+ Python suppoerts a mix of non-primitive data structures such as:
 + List
 + Tuple
 + Set
 + Dictionary
 


### List
+ A declaration within a square bracket separated by comma
+ Lists are mutable, i.e. you are  able to insert elements into it
+ Useful for manipulating a set of data e.g. adding/removing elements or sorting
+ Index element starts from 0
+ If you convert a string (word) to list, it will split them into single characters


```python
names = ['Ben', 'David', 'Kent', 'mimi']
print('Type: {}'.format(type(names)))
print('Names: {}'.format(names))
print('First Element in names  : {}'.format(names[0]))
print('Second Element in names : {}'.format(names[1]))
```

    Type: <class 'list'>
    Names: ['Ben', 'David', 'Kent', 'mimi']
    First Element in names  : Ben
    Second Element in names : David
    


```python
fruit = list('apple')
print('Fruit: {}'.format(fruit))
```

    Fruit: ['a', 'p', 'p', 'l', 'e']
    

### List Manipulation


```python
names = ['mimi',26, 'kent', 25, 'ben', 28, 'mnlee', 29]
print('Names: {}'.format(names))
print('First Element in names                      : {}'.format( names[0] ))
print('First to fourth Element in names            : {}'.format( names[0:4] ))

```

    Names: ['mimi', 26, 'kent', 25, 'ben', 28, 'mnlee', 29]
    First Element in names                      : mimi
    First to fourth Element in names            : ['mimi', 26, 'kent', 25]
    

List format [element_to_start, element_to_end, traversal]. Therefore:
+ [-1:-5:-1]
 + Start from the last index (-1), end at the (-5th) index, traverse backward every element (-1)
+ [0:8:2]
 + Start from the first index (0), end at the (8th) index, traverse forwards every 2nd element (2)


```python
print('Only the names in the list                  : {}'.format( names[0:8:2] ))
print('First to fourth Element in names (reverse)  : {}'.format( names[-1:-5:-1] ))
```

    Only the names in the list                  : ['mimi', 'kent', 'ben', 'mnlee']
    First to fourth Element in names (reverse)  : [29, 'mnlee', 28, 'ben']
    


```python
fruits = ['apple','banana','apple']
print('Fruits                               : {}'.format(fruits))

fruits.append('durian')
print('Added "durian" to Fruits             : {}'.format(fruits))

fruits.extend(['orange','peach'])
print('Added a list(orange, peach) to Fruits: {}'.format(fruits))

# Append VS Extend
# Append adds an object to the end of a list 
# Extend adds an iterable object to the end of a list
```

    Fruits                               : ['apple', 'banana', 'apple']
    Added "durian" to Fruits             : ['apple', 'banana', 'apple', 'durian']
    Added a list(orange, peach) to Fruits: ['apple', 'banana', 'apple', 'durian', 'orange', 'peach']
    ['apple', 'banana', 'apple', 'durian', 'orange', 'peach']
    


```python
fruits = ['apple','banana','cucumber']
print('Fruits                                : {}'.format(fruits))

fruits.insert(0,'carrot')
print('Add "carrot" at the front (index [0]) : {}'.format(fruits))

fruits.remove('apple')
print('Remove "apple" from list              : {}'.format(fruits))

fruits[2] = 'pear'
print('Change "cucumber" to "pear" in list   : {}'.format(fruits))

del fruits[1]
print('Delete 2nd entry - banana   from list : {}'.format(fruits))

fruits.pop()
print('Remove last entry from list with pop  : {}'.format(fruits))


```

    Fruits                                : ['apple', 'banana', 'cucumber']
    Add "carrot" at the front (index [0]) : ['carrot', 'apple', 'banana', 'cucumber']
    Remove "apple" from list              : ['carrot', 'banana', 'cucumber']
    Change "cucumber" to "pear" in list   : ['carrot', 'banana', 'pear']
    Delete 2nd entry - banana   from list : ['carrot', 'pear']
    Remove last entry from list with pop  : ['carrot']
    


```python
fruits = ['apple','banana','apple']
print('Fruits       : {}'.format(fruits))
print('Searching and deleting "apple" from list...')

num = 0
for fruit in fruits:
    if 'apple' in fruit:
        del fruits[num]
    num +=1
print('Output       : {}'.format(fruits))

```

    Fruits       : ['apple', 'banana', 'apple']
    Searching and deleting "apple" from list...
    Output       : ['banana']
    

### Nested List


```python
fruits = ['apple', [1,2,3], [4,5,6,7], 'pear', 'carrot']
print('Show 2nd index of list                   : {}'.format(fruits[1]))
print('Show 3rd element from 2nd entry of list  : {}'.format(fruits[1][2]))
print('Show 4th element from 3rd entry of list  : {}'.format(fruits[2][3]))
```

    Show 2nd index of list                   : [1, 2, 3]
    Show 3rd element from 2nd entry of list  : 3
    Show 4th element from 3rd entry of list  : 7
    

## Tuples
+ A declaration within brackets separated by comma
+ Tuples are immutable, i.e. you are not able to insert elements into a tuple
+ Useful in cases where you need to provide data but do not want it to be changed
+ Index element starts from 0


```python
names = ('ben', 'rais', 'kent', 'mimi', 'mnlee')
print('Type: {}'.format(type(names)))
print('Names: {}'.format(names, ))

print('3rd element in tuple: {}'.format(names[2]))
```

    Type: <class 'tuple'>
    Names: ('ben', 'rais', 'kent', 'mimi', 'mnlee')
    3rd element in tuple: kent
    


```python
# You cannot change contents within a tuple!
names[1] = 'boo'
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-94-15c974aea843> in <module>()
          1 # You cannot change contents within a tuple!
    ----> 2 names[1] = 'boo'
    

    TypeError: 'tuple' object does not support item assignment


## Set
+ A declaration within curly brackets separated by comma
+ Sets are mutable, i.e. you are  able to insert elements into it
+ Holds **unique** values only


```python
a = {1, 2, 3, 4, 5}
b = {2, 4, 6, 8}
c = {3, 6, 9}

print('Set a: {}'.format(a))
print('Set b: {}'.format(b))
print('Set c: {}'.format(c))

print('Elements that exists in a AND b    : {}'.format(a & b))
print('Elements that exists in b AND c    : {}'.format(b & c))

print('Unique elements in a AND b         : {}'.format(a | b))
print('Unique elements in b AND c         : {}'.format(b | c))

print('Elements that exists in a but NOT b: {}'.format(a - b))
print('Elements that exists in b but NOT c: {}'.format(b - c))


```

    Set a: {1, 2, 3, 4, 5}
    Set b: {8, 2, 4, 6}
    Set c: {9, 3, 6}
    Elements that exists in a AND b    : {2, 4}
    Elements that exists in b AND c    : {6}
    Unique elements in a AND b         : {1, 2, 3, 4, 5, 6, 8}
    Unique elements in b AND c         : {2, 3, 4, 6, 8, 9}
    Elements that exists in a but NOT b: {1, 3, 5}
    Elements that exists in b but NOT c: {8, 2, 4}
    

## Dictionary
+ A key-value pair declaration within curly braces
+ Useful in cases where you need to associate values to a specific tag (key)


```python
emp_info = { 1234: 'surendra', 2345: 'some one', 3456: 'cat body'}

print('Dictionary emp_info: {}'.format(emp_info))
print('emp_info of 2345   : {}'.format(emp_info[2345]))

print('Keys in emp_info   : {}'.format(emp_info.keys()))
print('Values in emp_info : {}'.format(emp_info.values()))

print('Items in emp_info  : {}'.format(emp_info.items()))
```

    Dictionary emp_info: {1234: 'surendra', 2345: 'some one', 3456: 'cat body'}
    emp_info of 2345   : some one
    Keys in emp_info   : dict_keys([1234, 2345, 3456])
    Values in emp_info : dict_values(['surendra', 'some one', 'cat body'])
    Items in emp_info  : dict_items([(1234, 'surendra'), (2345, 'some one'), (3456, 'cat body')])
    


```python
emp_info = { 1234: 'surendra', 2345: 'some one', 3456: 'cat body'}

print('Dictionary emp_info  : {}'.format(emp_info))

emp_info[8888] = 'new world'
print('Add emp_info 8888    : {}'.format(emp_info))

del emp_info[8888]
print('Delete emp_info 8888 : {}'.format(emp_info))

```

    Dictionary emp_info  : {1234: 'surendra', 2345: 'some one', 3456: 'cat body'}
    Add emp_info 8888    : {1234: 'surendra', 2345: 'some one', 3456: 'cat body', 8888: 'new world'}
    Delete emp_info 8888 : {1234: 'surendra', 2345: 'some one', 3456: 'cat body'}
    

### Summary
+ List has more 'features', hence if your list is large, consumes more memory
+ Tuple is constant, immutable so uses a set amount of resource
+ For security (constant), consider using tuple, otherwise list is advantageous due to its flexibility
+ Dictionary should be used when you need to store a value matching to a tag (key) such as telephone book. No other data structure enables this.

## Loops


```python
for alpha in 'boy cat':
    print(alpha)

print('\n')
for i in [1,2,3,4]:
    print(i)

print('\n')
set_a = {5, 3, 2, 1}
for ele in set_a:
    print(ele)
```

    b
    o
    y
     
    c
    a
    t
    
    
    1
    2
    3
    4
    
    
    1
    2
    3
    5
    


```python
dict_a  = { 'a': 'apple', 'c': 'cat', 'b': 'bat', '1': 'one'}
for key, value in dict_a.items():
    print('key is {}, fruit is {}'.format(key, value))
```

    key is a, fruit is apple
    key is c, fruit is cat
    key is b, fruit is bat
    key is 1, fruit is one
    


```python
import collections
od = collections.OrderedDict(sorted(dict_a.items()))    
for k,v in od.items():
    print('key is {}, fruit is {}'.format(k, v))

#for key, value in od.iteritems():
#    print('key is {}, fruit is {}'.format(key, value))
```

    key is 1, fruit is one
    key is a, fruit is apple
    key is b, fruit is bat
    key is c, fruit is cat
    


```python
a = 1
while a < 10:
    print(a)
    a += 1
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    


```python
# Flow Control: STOP, BREAK, CONTINUE
```


```python
while 1:
    name = input('Name: ')
    if '#' in name:
        break
    print ('Hello {}'.format(name))
```


```python
var = 10                    # Second Example
while var > 0:              
   var= var -1
   if var == 5:
      continue
   print (var)




```

    9
    8
    7
    6
    4
    3
    2
    1
    0
    


```python
a = 0
while a < 10:
    a += 1
    if a == 5:
        continue
    print(a)
```

    1
    2
    3
    4
    6
    7
    8
    9
    10
    


```python
# Lambda
```


```python
add = lambda x,y : x + y
print (add(3,4))

mult = lambda x,y : x * y
print(mult(3,4))
```

    7
    12
    


```python
numbers = [1,2,34,7,9,4]
factor2 = [x for x in numbers if x % 2 == 0]
print(factor2)

names = ['Bob','John','Peter','JaNE']
names = [x.title() for x in names]
print(names)

names = [x.lower() for x in names]
print(names)

names = [name for name in names if 'e' in name]
print(names)
```

    [2, 34, 4]
    ['Bob', 'John', 'Peter', 'Jane']
    ['bob', 'john', 'peter', 'jane']
    ['peter', 'jane']
    


```python
a = float(input("current temperature: "))
```

    current temperature: 1
    


```python
assert a > 17 and a < 45, "can't breathe"
```


    ---------------------------------------------------------------------------

    AssertionError                            Traceback (most recent call last)

    <ipython-input-11-6e401f7c13a7> in <module>()
    ----> 1 assert a > 17 and a < 45, "can't breathe"
    

    AssertionError: can't breathe



```python
a = input('pin number: ')
```

    pin number: 6
    


```python
if len(a) < 4:
    raise AttributeError
else:
    print("YAY")
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-6-d526941ecd79> in <module>()
          1 if len(a) < 4:
    ----> 2     raise AttributeError
          3 else:
          4     print("YAY")
    

    AttributeError: 



```python
# Functions
```


```python
def fans(name):
    print ('your name is:', name)
    num = len(name)
    print (' your fans number is %d' % (num))
    return name, num
```


```python
fans('Ben')
(x,y) = fans('Ben')
print(x)
print(y)

fans(name='Peter')
```

    your name is: Ben
     your fans number is 3
    your name is: Ben
     your fans number is 3
    Ben
    3
    your name is: Peter
     your fans number is 5
    




    ('Peter', 5)




```python
def sum (*numbers):
    total_sum = 6
    for num in numbers:
        total_sum += num
    return total_sum
```


```python
a = sum(1)
print(a)

a = sum(1,2,3,4)
print(a)

num_in = (1,2,3,4,5,6)
b = sum(*num_in)
print(b)
```

    7
    16
    27
    


```python
map_dict = {'surendra': 1234, 'ben' : 3456, 'unknwn': 4567}
```


```python
def display(**names):
    for k, v in names.items():
        print('name: {}, id: {}'.format(k,v))
```


```python
display(**map_dict)
```

    name: surendra, id: 1234
    name: ben, id: 3456
    name: unknwn, id: 4567
    


```python
def add(x ,y=5, *rem_ele, **names):
    age = x + y
    total_sum = 6
    for sum in rem_ele:
        total_sum += sum
    for key, value in names.items():
        print(key, value)
    print('total sum is {}'.format(total_sum))
```


```python
add(3)
```

    total sum is 6
    


```python
dict_a = { 'a': 'apple'}
add(3, 4, **dict_a)
```

    a apple
    total sum is 6
    


```python
numbers = [1,2,3,4,166]
add(3, 4, *numbers, **dict_a)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-3-6eabe31cbebd> in <module>()
          1 numbers = [1,2,3,4,166]
    ----> 2 add(3, 4, *numbers, **dict_a)
    

    NameError: name 'add' is not defined



```python
123
```




    123


