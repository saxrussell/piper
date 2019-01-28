## Booleans

We can use them explicitly or implicitly. Take the following code for example:

```python
# True and False can be explicitly used without first being assigned to a variable
while True:
    # do stuff

# there's nothing stopping us from assigning it to a variable first, though
my_bool = True

while my_bool:
    # do some stuff
    # if we don't have some sort of termination condition that sets my_bool = False , this while loop will go on forever

# an implicit use of a Boolean is where we perform an operation based on whether or not a condition evaluates to true or false. 
# in the example below, the expression (x > y) will be evaluated when the code executes and result in either True or False.

if x > y:
    # execute the code here when the value of x is greater than the value of y
else:
    # do something different when the value of x is not greater than the value of y
```

The `if` keyword will evaluate the expression `x > y` and the result of that evaluation will either be True or False, depending on what values are assigned to variables `x` and `y`.