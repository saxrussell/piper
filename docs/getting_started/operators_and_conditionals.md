# Operators and Conditionals

Code doesn't help us much if we don't have control over when it executes. To be useful, our code needs a way to determine when to perform the actions we want, under the specific conditions we determine. The `if` keyword is the most commonly used of a handful of conditional controls available, and its use is pretty intuitive - if (some_condition), do this other thing.

```python
if 2 == 2:
    print("yep, 2 does equal 2")
```

That double equals `==` is an operator; specifically, it's a comparison operator. Python has a variety of operators; some are used to compare values while others are used to assign values. W3 has a nice, easy page about operators here: https://www.w3schools.com/python/python_operators.asp

At the end of the day, all that `if` will do is return a boolean (`True` or `False`) based on the condition statement. That part is easy to understand. Crafting the conditional statement is where humans get themselves into trouble because logic is hard.

## Logical Operators

As you start to solve more interesting problems with your code, you'll need more complex conditions.

Take the following example:

```python
im_hungry = True
the_time = 1730
time_to_eat = 1800

if im_hungry and the_time >= time_to_eat:
    lets_eat = True
else
    lets_eat = False
```

The code reads almost exactly how most people think about a problem, "If I'm hungry and it's dinner time, I'll go eat.Otherwise, I won't." The kicker being that `and` operator. It's a logical operator that adds a condition for `if` to evaluate. Using `and` is an _inclusive_ operation, meaning that `if` will only return `True` if **both** conditional statements each evaluate to `True`. In the example above, what will `lets_eat` evaluate to?

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
