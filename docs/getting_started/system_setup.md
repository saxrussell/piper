# First Steps

Instead of jumping through all the hoops of setting up the Raspberry Pi as a development machine, we are going to use your Windows laptop.

1. Install VS Code (a fancy text editor)
    download link: https://code.visualstudio.com/#alt-downloads
    check all the checkboxes during the installer wizard

2. Install Python (at the end of the day, it's a program just like anything else)
    download link: https://www.python.org/downloads/

3. Install Git (don't worry too much about this, yet. just needed to fetch all of the files in this repository, if you want them.)
    download link: https://git-scm.com/download/win
    The download page should automatically start the correct download for your system, but if it doesn't, choose the "32-bit Git for Windows Setup" link.

# Start and Configure VS Code

Once it starts, you'll want to install some extensions and change some settings to help you write code more effectively.

Press the hotkey combination `Ctrl Shift X` to open the Extensions menu on the left. At the top, type Python into the search field, click the little green "Install" button. Once the plugin is installed, the little green install button turns into a little blue "Reload" button. Click it to finish the installation. There are some other plugins we'll end up installing later, but for now, this should be good enough.

It's also a good idea to turn on the "autosave" setting. Nothing is worse than losing work because you forgot to save. Press the hotkey combination `Ctrl ,` to open the general settings editor. At the top, there's a search field where you can type in keywords to look for. Type `autosave` in the search field. If you pause for a second, you don't even have to press `Enter` for the page to change and only show the results of your search. The top result should be `Files: Auto Save`, under which is a dropdown menu that provides the autosave options available to you. From that dropdown, select `onFocusChange`. You can then close the `Settings` tab at the top of your editor. Settings are updated immediately and automatically...no need to click a `Save` or `Apply` button. Now your work will be automatically saved any time the focus context switches (when you switch between open files, menus, or windows).

# Using the Python interpreter

Python is an interpreted language which means that we, as programmers, don't have to perform an explicit compiling step like we would have to in languages like C, Go, or Java. We can execute our code immediately after we write it and the compilation will happen on-the-fly. Python does this by using a program called an interpreter to translate the Python code you write into compiled bytecode to be processed by the assembler (more on that later). You can even run the interpreter directly from the Start menu (or from a PowerShell console) to write and execute Python code in real time just like using a terminal.

Go ahead and run Python from the Start menu. A black, terminal-looking window will open that looks like:

```
Python 3.7.2 (tags/v3.7.2:9a3ffc0492, Dec 23 2018, 22:20:52) [MSC v.1916 32 bit (Intel)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

From here, you can write and execute python code directly. This isn't usually how we would run **finished** Python code, but it is a handy and powerful tool for experimenting and learning. Since we went through all the trouble of installing and setting up VS Code, we won't be doing much with the interpreter just yet, so go ahead and close the window...just remember that it's there because we'll be using it in later exercises.

# Writing Code in a File

Pretty much what it says...instead of writing instructions directly into the interpreter, we save them in a file and then "pass" that file to the interpreter to be run. Let's make a new file, now. On the left, click the "Explorer" icon at the top of the menu icon list. Right-click the "piper" directory and click New File. Name the file datatypes.py and press enter. The new file will open up in the editor and you're ready to start writing code!
