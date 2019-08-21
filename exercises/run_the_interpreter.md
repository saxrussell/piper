# Using the Python Shell

Before we write any code into files, lets start with using the Python shell
directly. This will allow us to write and execute Python expressions in
real-time and is the easiest way to learn the basics. On Windows, you can access
the Python shell by running the `Python` executable from the start menu or, if
you have an open Powershell window, by typing `python` and pressing enter. 

Once on the python command line, anything you type will be interpreted as python
code.

Example 1:

```python
print("Hello, there!")
```

In the example above, `print` is a built-in function. The content of the
parentheses are _arguments_ (also refered to as input parameters) passed to the
function for use in whatever that function does. Kinda like math functions. The
classic `f(x)` is pretty much the same thing...`f` is the function and `x` is
the parameter passed to that function.

It would be tedious to always have to re-type things in our code when we want to
vary the output. We code because we want the computer to do stuff for us, not
the other way around.

Example 2:

```python
my_string = "Hello, there!"
print(my_string)
```

`my_string` is a _variable_. Variables are how we define _objects_. When we set
a variable like in the example above, its value is stored in memory while our
program is running. If we want to change the value of that variable, we can do
so at any time later in our code.

Above, we set the `my_string` variable to whatever it is we want to output and
then use the variable name as agrument to the `print` function. The output will
be the same, but we are a step closer to having code that serves us instead of
us serving it.

```python
my_string = "Hello, there!"
my_string = "Bye, now!"

print(my_string)
```

Python code executes from top to bottom in a file. If a variable is set more
than once in a given program, the last declaration "wins."

This is all very interesting, but we would still have to repeat ourselves in
code multiple times to change the output produced. Wouldn't it be much more
efficient to just have the program ask us what we wanted when we run it?

```python
my_string = input("What would you like to say? : ")
print(my_string)
```

You can run the above code as many times as you like and enter different input
each time without having to change any code! The rest of programming is, for the
most part, just iteration on this theme; take repetative tasks and make a tool
that alleviates the toil of performing those tasks.
