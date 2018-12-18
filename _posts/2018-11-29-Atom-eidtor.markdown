---
title:  Atom for Pythonist  
description: Atom the wonderful free editor
excerpt: Atom is a free and open-source text and source code editor for macOS, Linux, and Microsoft Windows with support for plug-ins written in Node.js, and embedded Git Control, developed by GitHub.
header:
    overlay_filter: "0.1"


categories:
  - wilt
tags:
  - Atom
  - editor
---


<figure>
  <img src="/assets/images/2018-11-29-Atom-eidtor/0_Atom.png" alt="Atom to downloaded">
  <figcaption> Atom: A hackable text editor for the 21st Century </figcaption>
</figure>


[Atom](https://atom.io) is a free and open-source text and source code editor for macOS, Linux, and Microsoft Windows with support for plug-ins written in Node.js, and embedded Git Control, developed by GitHub ([Wikipedia](en.wikipedia.org/wiki/Atom_(text_editor))).

>Atom was launched in February 2014 by the GitHub team.

A hackable text [editor](https://atom.io) for the 21st Century created by GitHub team which is simple, powerful and highly customizable.


[Download](https://atom.io) for 32 bit or 64-bit installer according to your operating system. Once it is downloaded, go to the download folder and double-click on “AtomSetup-x64.exe” for installing it.
<figure>
  <img src="/assets/images/2018-11-29-Atom-eidtor/1_1_download_Atom.png" alt="Atom to downloaded">
  <figcaption> AtomSetup-x64.exe </figcaption>
</figure>

Click on the icon and install the editor as shown below:
<figure>
  <img src="/assets/images/2018-11-29-Atom-eidtor/2_Installation_Atom.png" alt="Install Atom">
  <figcaption> Installing Atom </figcaption>
</figure>

After giving the permission to the windows, a beautiful image will appear with the caption “Atom is being installed. It will launch once it is done”.
<figure>
  <img src="/assets/images/2018-11-29-Atom-eidtor/3_installing_step_Atom.png" alt="Install Atom">
  <figcaption> Atom editor </figcaption>
</figure>

Once it is installed, an icon on the desktop will appear. To use Atom, either click on the desktop icon or find the “Atom” in the start menu.  

---


## Atom for Pythonist ##

Pythonist loves Atom as both are open source. By doing some changes Atom could be customized for Pythonist.

We are going to install the following packages:

2. platform_ide-terminal
3. autocomplete-python
4. python-autopep8
5. linter-flake8
6. Browser Plus
7. file-icons

---

Let start installing the packages with some explanation.



### 1. platform_ide-terminal ###

It is a terminal package for Atom for integrating command line in ATOM.

Click on File> Settings>Install ``` "platform-ide-terminal"  ```

<figure>
  <img src="/assets/images/2018-11-29-Atom-eidtor/9_platform-ide-terminal.png" alt="install platform-ide-terminal">
  <figcaption> Installing platform-ide-terminal in Atom editor </figcaption>
</figure>


It stays at the bottom of the editor. Click on the "plus sign" on the bottom-left side for using it.

For more information click [here](https://atom.io/packages/platformio-ide-terminal).

<figure>
  <img src="/assets/images/2018-11-29-Atom-eidtor/10_platform-ide-terminal_final.png" alt="platform-ide-terminal">
  <figcaption> platform-ide-terminal in function </figcaption>
</figure>




> If you press Ctrl+T or Ctrl+P, the Fuzzy Finder will pop up. This will let you quickly search for any file in your project by typing parts of the path.


### 2. autocomplete-python ###

autocomplete-python will make your life more easy as python developer. It autocompletes python packages, variables, methods, and functions with their arguments in Atom.


Click on File>Settings>Install ```autocomplete-python```

<figure>
  <img src="/assets/images/2018-11-29-Atom-eidtor/11_autocomplete_python.png" alt="Install Atom">
  <figcaption> Installing autocomplete-python </figcaption>
</figure>


### 3. python-autopep8 ###

  It formats the python code according to the PEP8 guidelines. For more information click [here]( https://pypi.org/project/autopep8/).


  Click on the Settings of python-autopep8 and go to the Settings. Check the ```Format on Save``` as shown below.

  <figure>
    <img src="/assets/images/2018-11-29-Atom-eidtor/13_python-autopep8.png" alt="python-autopep8">
    <figcaption> Installing python-autopep8 </figcaption>
  </figure>

  * autopep8 need to be installed on the system. Open bash and type

  ```
     pip install autopep8
  ```

### 4. linter-flake8 ###


Flake8 is a Python library that wraps PyFlakes, pycodestyle and Ned Batchelder’s McCabe script. It is a great toolkit for checking your code base against coding style (PEP8), programming errors (like “library imported but unused” and “Undefined name”) and to check cyclomatic complexity. For more information click [here](https://simpleisbetterthancomplex.com/packages/2016/08/05/flake8.html)

<figure>
  <img src="/assets/images/2018-11-29-Atom-eidtor/14_linter-flake8.png" alt="python-autopep8">
  <figcaption> Installing linter-flake8 </figcaption>
</figure>

* flake8 need to be installed on the system. Open bash and type

    ```
      pip install flake8
    ```



### 5. Browser Plus ###

It opens a real browser in ATOM, which is very handy for debugging and checking the output at the same time. It opens the home page(maintained in the settings) or http://www.google.com.

  >   ctrl + shift + P and search Browser Plus for opening the browser window.

  <figure>
    <img src="/assets/images/2018-11-29-Atom-eidtor/15_broswer_plus.png" alt="python-autopep8">
    <figcaption>Installing Browser Plus </figcaption>
  </figure>


### 6.file-icons ###

  This put a little icon next to each file, which helps us to identify which kind of file it is.

  <figure>
    <img src="/assets/images/2018-11-29-Atom-eidtor/16_file_icons.png" alt="python-autopep8">
    <figcaption>file icons showing the file icon next to it </figcaption>
  </figure>

 File-specific icons in Atom for improved visual grepping.
  <figure>
    <img src="/assets/images/2018-11-29-Atom-eidtor/17_file_icons.png" alt="python-autopep8">
    <figcaption>file icons showing the file icon next to it </figcaption>
  </figure>
---

### Open File with Atom in one click ###

The normal procedure for opening a file or a directory with Atom is by first opening the editor Atom, with either of two methods as mentioned above. Then click on "File" > "Open folder" and browse to the file or the folder, which is a very cumbersome process as shown below:

<figure>
  <img src="/assets/images/2018-11-29-Atom-eidtor/4_open_folder.png" alt="Install Atom">
  <figcaption> Atom editor </figcaption>
</figure>

Wouldn’t it be amazing if we could just open the file in one click? So let see how we can do it.

1. Open the editor Atom
2. Click on File > Settings and Click "System" tab. Check the ```Show in file context menus``` and ```Show in folder context menus
``` as shown below:
3. Close the editor Atom.


<figure>
  <img src="/assets/images/2018-11-29-Atom-eidtor/5_open_with_Atom.png" alt="Install Atom">
  <figcaption> Atom’s System tab </figcaption>
</figure>



Right click and "open with Atom" option will appear as shown below. Atom is available with just a right click away.

<figure>
  <img src="/assets/images/2018-11-29-Atom-eidtor/6_rightopen_with_Atom.png" alt="Install Atom">
  <figcaption> Open with Atom option available on right click </figcaption>
</figure>
---

## Conclusion ##
We have learned about a wonderful open source editor called Atom. How it is being used by Pythonist and some tricks and tips about using it.

---

REFERENCE
1. [wikipedia](en.wikipedia.org/wiki/Atom_(text_editor))
2. [Atom](https://atom.io)
3. [platform-ide-terminal](https://atom.io/packages/platformio-ide-terminal)
4. [python-autopep8](https://pypi.org/project/autopep8/)
5. [linter-flake8](https://simpleisbetterthancomplex.com/packages/2016/08/05/flake8.html)
