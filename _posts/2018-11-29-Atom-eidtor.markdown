---
title:  Atom
description: Atom the wonderful free editor
categories:
  - Post
tags:
  - Atom
  - editor
---

Atom


Atom is a very powerful editor.


Go to the official webpage of Atom(https://atom.io) and download the Atom for 64 bit installer.

Install the Atom. Wait until Atom is installed.

Normally to open Atom, we browse to the program and click on the Atom icon which opens in a random directory.


Is it cool if we can open the Atom in any directory without changing the directory all the time.

For this we have to some changes.
1. Open Atom
2. Click on File > Settings and Click "System" tab.
    Check the second and third options.
      Show in file context menus
      Show in folder context menus

3. Close Atom

Right click and you will see "open with Atom".
Now you can open the Atom anywhere you want to open.


Make Atom ready for Python

1. File > Settings > Install
then search "script" and install it.

it will let the python file to run from the Atom.
Write a code in python and then use keyboard shortcuts Ctrl + shift + b for windows and unix.

2.  There are other ways also. Where we can integrate command line in ATOM so that we don't need other windows for command line.
  File> Settings>Install
  "platform-ide-terminal"
On the left side there will be a "plus" sign. click on it and a new command line window will appear.


If you press Ctrl+T or Ctrl+P, the Fuzzy Finder will pop up. This will let you quickly search for any file in your project by typing parts of the path.


3. File>Settings>Install another package
  a. "autocomplete-python".
  This will make your life more easy as python developer.

  b. "python-autopep8"
  this format the python code according to the PEP8 guidelines. more information could be find here https://pypi.org/project/autopep8/

      1. to use this we need to install autopep8 by using pip install autopep8 in the bash
      2. Click on the Settings of python-autopep8 and go to the Settings. check the format on Save


  c. "linter-flake8"


    Flake8 is a Python library that wraps PyFlakes, pycodestyle and Ned Batchelder’s McCabe script. It is a great toolkit for checking your code base against coding style (PEP8), programming errors (like “library imported but unused” and “Undefined name”) and to check cyclomatic complexity.
    https://simpleisbetterthancomplex.com/packages/2016/08/05/flake8.html

    1. To use this plugin flake8 will need to be installed on your system.
      pip install flake8 from the bash


  d. "Browser Plus"
     Install this. It opens a real browser in ATOM. Which is very handy for debugging and checking the output at the same time.
     ctrl+shift+p(cmd+shift+p) Browser Plus: Open. It opens the home page(maintained in the settings) or http://www.google.com.
     ctrl + shift + P to open the browser window.

  e . "file-icons"
  This put a little icon next to each file, which helps us to identify which kind of file it is. File-specific icons in Atom for improved visual grepping.
