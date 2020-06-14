# Operators and Conditionals

Code doesn't help us much if we don't have control over when it executes. To be useful, our code needs a way to determine when to perform the actions we want, under the specific conditions we determine. The `if` keyword is the most commonly used of a handful of conditional controls available, and its use is pretty intuitive - if (some_condition), do this other thing.

```python
if 2 == 2:
    print("yep, 2 does equal 2")
```

That double equals `==` is an operator; specifically, it's a comparison **operator**. Python has a variety of operators; some are used to compare values while others are used to assign values. W3 has a nice, easy page about operators here: https://www.w3schools.com/python/python_operators.asp

At the end of the day, all that `if` will do is return a boolean (`True` or `False`) based on the condition statement. That part is easy to understand. Crafting the conditional statement is where humans get themselves into trouble because logic is hard.

## Boolean Logic

There's a lot going on above that intuitively makes sense, but that inuition breaks down fast outside of simple comparisons. Just gonna take a minute to dive through some Boolean logic evals. We're looking for truth. It's a binary mode of thinking and there is NEVER any ambiguity. One way or another, the machine will reach a single, incontrovertible answer, and it will break your brain at some point.

```
print(True == True)
True

print(True == False)
False

print(False == False)
True

print(False == False == True)
False

print((False == False) == True)
True

print(True and False == True)
False

print(True and False == False)
True

print(True or False == False)
True

print(True or False == True)
True
```

Context matters in these evaluations, so using parentheses allows for defining order of operations (just like in high school math class). You can use the Python interpreter to play with these evaluations until it makes sense, but the major point for someone just starting out with code is to try and keep your conditions as simple as possible. It makes for more stable, readable code, and prevents cognitive burnout.

We can use Booleans directly or as variable values. Depending on what you're writing or who you're writing it for, each approach is perfectly valid. Personally, I prefer assigning values to variables since naming the variable something appropriate helps other team members (or even myself, if I'm picking up a project I haven't worked on in awhile) understand what it represents in context. Take the following code for example:

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

## Logical Operators

As you start to solve more interesting problems with your code, you'll need more complex conditions. Defining the conditions requires a comparison **operator** in between two expressions, but what happens when a single value isn't enough to make a decision?

Take the following example:

```python
im_hungry = True
the_time = 1730
time_to_eat = 1800

if im_hungry and the_time >= time_to_eat:
    print("Dinner time!")
else
    print("Eh, not ready to eat yet.")
```

The code reads almost exactly how most people think about a problem, "If I'm hungry and it's dinner time, I'll go eat. Otherwise, I won't." If the expression between the `if` keyword and the colon `:` at the end of the line evaluates to `True`, do the stuff on the next, indented line(s). The `else` keyword (important that it has the same indentation as `if`) indicates an alternative action if the expression evaluates to `False`. This is totally optional if your context doesn't require it. If you don't care about having a print statement for "not dinner time" or whatever, it's perfectly valid to just do something like:

```python
if im_hungry and the_time >= time_to_eat:
    print("Dinner time!")
```

In which case, if the condition evaluates `False`, the interpreter just moves along without printing the "Dinner time!" string to the terminal.

Anyway, the big thing to pay attention to is that `and` operator. It's a logical operator that adds a condition for `if` to evaluate. Using `and` is an _inclusive_ operation, meaning that `if` will only return `True` if **both** conditional statements each evaluate to `True`. In the example above, what will `lets_eat` evaluate to?

Stepping through evaulating each expression:

- `im_hungry == True` so, `True == True`
- Because we used the `and` operator, `if` knows there are more evaluations to be done.
- The entire expression `the_time >= time_to_eat` is evaluated for its result. `(1730 >= 1800) == False`
- The colon `:` character denotes the end of the `if` condition, so the final expression to evaluate comes down to `True and False`

Since `True and False` evaulates to `False`, and we have an `else` defined, the output will be:

```
Eh, not ready to eat yet.
```

Let's change the scenario slightly. What if the above problem involved sadistic parents who don't care if you're hungry when dinner time rolls around and will make you eat dinner because it's dinner time? In that case, if **either** condition is met, you're going to eat. For this scenario, the logical operator `or` is required.

```python
if im_hungry or the_time >= time_to_eat:
    print("Dinner time!")
else
    print("Eh, not ready to eat yet.")
```

What will the output be?
