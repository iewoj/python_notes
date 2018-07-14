
# Basic Exercises

## Write a basic program to check for the correct password        


```python
import getpass

while 1:
    read = getpass.getpass('Enter password:')
    if read == 'P@ssw0rd':
        print('Login successful.')
        break
```

    Enter password:········
    Enter password:········
    Enter password:········
    Login successful.
    

## Write a basic program to take in items into a shopping cart


```python
shopping_cart = []
while 1:
    read = input('Enter item into cart (type DONE to exit):')
    if 'done' in read.lower():
        print('Complete shopping cart  : {}'.format(shopping_cart))
        break
    else:
        shopping_cart.append(read)
        print('Shopping_cart items     : {}'.format(read))
```

    Enter item into cart (type DONE to exit):milk
    Shopping_cart items  : milk
    Enter item into cart (type DONE to exit):cookies
    Shopping_cart items  : cookies
    Enter item into cart (type DONE to exit):DONE
    Final shopping cart  : ['milk', 'cookies']
    

## Write a basic program to take in 3 meetings (subject & agenda)


```python
meeting_dict = {}
a = 1
while a <= 3:
    meet_subject = input('Enter meeting subject:')
    meet_agenda  = input('Enter meeting agenda :')
    meeting_dict[meet_subject] = meet_agenda
    a += 1

for k in meeting_dict:
    print('Meeting subject: {}, agenda: {}'.format(k,meeting_dict[k]))
    
```

    Enter meeting subject:Product Sprint #1
    Enter meeting agenda :Team discussion
    Enter meeting subject:Milestone meet up
    Enter meeting agenda :Boring items
    Enter meeting subject:Weekly Gap Closure 
    Enter meeting agenda :Closing my 5 open items!
    Meeting subject: Product Sprint #1, agenda: Team discussion
    Meeting subject: Milestone meet up, agenda: Boring items
    Meeting subject: Weekly Gap Closure , agenda: Closing my 5 open items!
    
