# Variables

When starting out, the code we're going to write will operate on static values, since that's the easiest way to introduce some of the basic concepts. In practice, that's not very useful since we don't want to write new code for every possible value we want to operate on. A basic example is adding two numbers.


We *could* write our addition expression like:
```python
print(1+1)
# output: 2
```

But then we would have to write the same code over again, with different values, to evaluate other combinations of numbers to add. 
```python
print(1+1)
# output: 2
print(1+2)
# output: 3
print(2+3)
# output: 5
print(3+5)
# output: 8
print(5+8)
# output: 13
```
The point of writing code is to automate repetative tasks like this, so it doesn't make much sense to work with code this way. The first step in writing repeatable code is to create an expression that can be resused, just like we do in algebra. Also like we do in algebra, we use **variables** to represent the different elements we want to operate on.

A single `=` is the assignment operator in Python. The name of the variable can be anything you want it to be. In the example below, I've used the (boring) names `x` and `y`, but could have just as easily named them `barney` and `rubble`. While it can be fun to choose silly variable names, doing so usually detracts from the readability of your code and makes it more difficult for your own brain to keep track of the context in which those variables are being used. The general convention is to use variable names that are short, but descriptive enough to understand, at a glance, what their purpose is.

```python
x = 8
y = 13
print(x + y)
# output: 21
```

This first step still hasn't bought us much, but it does pave the way to use other operations that will, such as [loops](#flow-control) or [functions](#functions), which will *change* the value of each variable for every iteration of the "add numbers" operation.

```python
for i in range(0, 10):
    x = i + 1
    y = i + 2
    print(x + y)
```
```
Output:
3
5
7
9
11
13
15
17
19
21
```

Don't worry if you don't understand what just happened there entirely. Despite the code being short, there's a lot going on. The important part to understand is that we used variable substitution to perform a series of calculations without having to write the individual math expressions for each pair we wanted to add.

# Data Types

We write code to manipulate data. This data can take many forms, and many are shared between programming languages. 

## Primitives

All programming languages have a set of basic data types, or "primitives", which we use as the building blocks of our code. These primitives are shared among almost all modern programming languages (we can get into the reasons for this later) and tend to be treated identically between those languages, as well.

Python has four primitive types:

- String
- Integer
- Float
- Boolean

### String 

A string is a sequence of characters. Basically, it's text. What you're reading right now is a string. Strings can be zero or more characters and are wrapped in either single or double quotes.

```python
# this is a comment string. it is ignored by the interpreter and can be written in line within your python file
# we use comment lines and blocks to make notes in our code, about our code, in plain English.

'''
this is a comment block.
Just like a comment string, it is ignored by the interpreter so you can write whatever you want.
you can have multiple lines within the two sets of
triple quotes
'''

"""
this is also
a comment block.
the difference between triple single-quote characters
and triple double-quote characters is purely conventional and has
no functional impact.
"""
```
If the comments are all that's in your Python code, executing it will do nothing. If you want output from your code, you have to use a function that will do it for you. The `print()` function is a commonly-used function to use while developing your code to check that your program is delivering the behavior you expect.

```python
# write a string to the terminal without assigning it to a variable first
print("Hello, I am a string")
```
```
Output:
Hello, I am a string
```

```python
# double-quoted string assigned to a variable and written to the terminal by passing the string variable to the print() function
string_var = "this is a string"
print(string_var)
```
```
Output:
this is a string
```

```python
# same as above just using single-quotes
string_var = 'so is this'
print(string_var)
```
```
Output:
so is this
```

```python
"""
sometimes it's necessary to include the quote characters in the string. python makes this easy by letting us use the alternative quote character,
from the one used to start the string, without using an escape character first (more on that later)
"""
string_var = 'If I need "double-quote" characters in my string, I wrap my string in single-quotes'
print(string_var)
```
```
Output:
If I need "double-quote" characters in my string, I wrap my string in single-quotes
```

```python
string_var = "Alternatively, if I need 'single-quote' characters in my string, I wrap my string in double-quotes"
print(string_var)
```
```
Output:
Alternatively, if I need 'single-quote' characters in my string, I wrap my string in double-quotes
```

Check out [the string examples](examples/strings) for more sample code of how strings can be used.

### Boolean

The Boolean type only has two potential values; True or False. Boolean values are how we make conditional determinations in a purely logical system. Using the interpreter is handy for demonstrating these concepts, so fire it up and see for yourself. The `==` is Python's equivalence operator (different than the `=` assignment operator). Operators are significant and have their own section later in this guide, but feel free to jump over there and look up any of the operators used in the following examples.

```python
>>> True == True
True

>>> True == False
False

>>> False == False
True

>>> 2 + 2 == 4
True

>>> 2 + 2 == 5
False

# both expressions must evaluate to True
>>> 2 + 2 == 4 and 3 + 3 == 6
True

>>> 2 + 2 == 5 and 3 + 3 == 6
False

# one expression must evaluate to True
>>> 2 + 2 == 5 or 3 + 3 == 6
True

>>> 2 + 2 == 5 or 3 + 3 == 9
False

# use parentheses to declare which expressions are evaluated first. just like math, parentheses are evaluated from inside to outside
>>> (2 + 2 == 4 or 3 + 3 == 6) and 4 + 4 == 8
True

>>> (2 + 2 == 10 or 3 + 3 == 4) and 4 + 4 == 8
False

>>> (True or (False == False and True == False)) or ((True == True and False == False) == True)
True
```

### Int

An `int` is any whole integer between negative infinite and infinite. We can perform arithmetic operations on integers, use them as iterators to loop over a collection. Note that we don't use quotation marks when writing integers.

```python
2 + 2
4

# try the same thing with strings and all you get is a single, concatenated string made of both individual "2" characters
 "2" + "2"
'22'

# the same order of operations rules apply here as they do in your math classes
# if you want a particular part of an expression evaluated first, wrap it in parentheses
>>> 2 + 2 + 2 + 6 * 4
30
>>> (2 + 2) + (2 + 6) * 4
36
>>> ((2 + 2) + (2 + 6)) * 4
48
```

An interesting note, and a good segue to the next primitive type, is the division operator when applied to integers. Take the arithmetic expression `8 / 4`. What would you expect the answer to be if you entered that into the Python interpreter?

```python
>>> 8 / 4
2.0
```

What the what? That result contains a decimal, which is not an `int`! An `int` is a whole number which, even if the digit to the right of the decimal is `0`, a decimal representation is **not**. What type is it, then?

```python
# you can determine the type of any object by calling the built-in type() function on it
type(8 / 4)
<class 'float'>
```

So, what's a float? 

### Float
Floats are floating point numbers; real numbers with a franctional component.

```python
>>> 5 * 1.45
7.25

>>> 7 / 3
2.3333333333333335
```

The problem with a lot of floating point numbers is precision. The second expression above results in an infinite number of decimal places, which is impossible to fit into memory because...ya know...infinite. Brain melting existential stuff. Anyways, `float` results are trimmed to 15 points of precision. Maybe 17, depending on whatever C compiler underpins your Python installation. If you need more than that, a number of libraries exist to help, but we'll cover that in a later section.

## Collections
TODO: Lists, tuples, dictionaries
