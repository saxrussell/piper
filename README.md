# First Steps

Instead of jumping through all the hoops of setting up the Raspberry Pi, we are going to use your Windows laptop.

1. Install VS Code (a fancy text editor)
    download link: https://code.visualstudio.com/#alt-downloads
    check all the checkboxes during the installer wizard

2. Install Python (at the end of the day, it's a program just like anything else)
    download link: https://www.python.org/downloads/

# Start VS Code

Once it starts, you'll want to install some extensions to help you write code more effectively.

Press the hotkey combination `Ctrl Shift X` to open the Extensions menu on the left. At the top, type Python into the search field, click the little green "Install" button. Once the plugin is installed, the little green install button turns into a little blue "Reload" button. Click it to finish the installation.

There are some other plugins we'll end up installing later, but for now, this should be good enough.


# Using the Python interpreter

Python is a language built on top of C. It uses a program called an interpreter to translate the python code your write into compiled bytecode. You can run the interpreter directly from the Start menu, or you can run it from a PowerShell console.

Go ahead and run Python from the Start menu. A black, terminal-looking window will open that looks like:

```
Python 3.7.2 (tags/v3.7.2:9a3ffc0492, Dec 23 2018, 22:20:52) [MSC v.1916 32 bit (Intel)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

From here, you can write and execute python code directly. This isn't usually how we would run "finished" or "prodcution-ready" Python code, but it is a handy tool for experimenting and learning. Since we went through all the trouble of installing and setting up VS Code, we won't be doing much with the interpreter just yet, so go ahead and close the window.

# Writing Code in a File

Pretty much what it says...instead of writing instructions directly into the interpreter, we save them in a file and then "pass" that file to the interpreter to be run. Let's make a new file, now. On the left, click the "Explorer" icon at the top of the menu icon list. Right-click the "piper" directory and click New File. Name the file datatypes.py and press enter. The new file will open up in the editor and you're ready to start writing code!

# Variables
TODO

# Data Types

We write code to manipulate data. This data can take many forms, and many are shared between all programming languages. 

## Primitives

### String 

A string is a sequence of characters. Basically, it's text. What you're reading right now is a string. Strings can be zero or more characters and are wrapped in either single or double quotes.

```python
"this is a string"
'so is this'

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

Check out [strings.py](type_examples/strings.py) for a few examples of how strings can be used.

### Boolean

The Boolean type only has two potential values; True or False. Booleans are how we make conditional determinations in a purely logical system. Take the following code for example:

```python
if x > y:
    # execute the code here
```

the `if` keyword will evaluate the expression `x > y` and the result of that evaluation will either be True or False, depending on what values are assigned to variables `x` and `y`.

### Int
### Float
### Complex

## Collections

# Functions

# Conditionals

# Flow Control

# Libraries, Modules, and Imports
