## Declaring Functions



```python
def get_employee(name):
    num = len(name)
    return name, num
```


```python
get_employee('Ben')
```




    ('Ben', 3)




```python
get_employee(name='Peter')
```




    ('Peter', 5)




```python
(nm,ln) = get_employee('Ben')
print ('My name is: {} and the length is: {}'.format(nm, ln))
```

    My name is: Ben and the length is: 3


When passing arguments to functions, you can pass it as is, or use \*args or \**kwargs. This accepts an arbitrary number of arguments.
+ The single asterisk is used to pass a non-keyworded, variable-length argument list,
+ The double asterisk form is used to pass a keyworded, variable-length argument list


```python
def sum (*numbers):
    total_sum = 6
    for num in numbers:
        total_sum += num
    return total_sum
```


```python
a = sum(1)
print('Return value: {}'.format(a))

a = sum(1,2,3,4)
print('Return value: {}'.format(a))

num_in = (1,2,3,4,5,6)
b = sum(*num_in)
print('Return value: {}'.format(a))
```

    Return value: 7
    Return value: 16
    Return value: 16



```python
def display(**names):
    for k, v in names.items():
        print('Name: {}, ID: {}'.format(k,v))
```


```python
map_dict = {'surendra': 1234, 'ben' : 3456, 'unknwn': 4567}
display(**map_dict)
```

    Name: surendra, ID: 1234
    Name: ben, ID: 3456
    Name: unknwn, ID: 4567



```python
def add(x, *rem_ele, **names):
    value = x**2
    total_sum = 6
    for sum in rem_ele:
        total_sum += sum
    for key, value in names.items():
        print('Printing from dictionary: KEY - {}, VALUE - {}'.format(key, value))

    print('Value of {}^2 = {}'.format(x, value))
    print('Total sum = {}'.format( total_sum))

```


```python
add(4)
```

    Value of 4^2 = 16
    Total sum = 6



```python
dict_a = { 'a': 'apple'}
add(3, 4, **dict_a)
```

    Printing from dictionary: KEY - a, VALUE - apple
    Value of 3^2 = apple
    Total sum = 10



```python
numbers = [1,2,3,4]
add(3, 4, *numbers, **dict_a)
```

    Printing from dictionary: KEY - a, VALUE - apple
    Value of 3^2 = apple
    Total sum = 20
    
