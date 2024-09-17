# URLs-Editor


## Introduction
The Code Repository for Python implementation of bookmarks by flet.
(For Japanese speakers.)

## Getting Started


### Install Requirments
Python >= 3.12 and
```
pip install -r requirements.txt
```
You can already get started.<br><br>
The setting.json is primarily a Ruff Extensions setting. Change it as necessary.


### Build
It can be run through python, but we recommend building it into an executable file.<br>The pre-built files are available on the [release page](https://github.com/MelsRoughSketch/URLs-Editor/releases/tag/v1.0.0), but if you want to change the code, ignore windows warnings, or run it on non-Windows environments, you can build it with the following command.
```
python -m nuitka --onefile --standalone --windows-console-mode=disable --follow-imports "URLs Editor.py"
```
Do not use the ```--windows-console-mode``` option when building for non-Windows environments. Instead, execute ```nuikta -h``` command to check the options for each OS and use them.<br>
Using Nuitka will create a lighter and faster application than a fret build, although the app icon will not be correctly configured.


## How To
### Execute
To execute from the command line, run the following command.
```
python "URLs Editor.py"
```
Of course, if you use an executable file, just click on it.


### Creating Bookmark Page
This script allows GUI manipulation of HTML \<Details\> tabs. Basically, all you have to do is create elements and paragraphs as you wish, and press the button labeled "この内容で反映する" at the end.<br><br>
The bookmark is named "URLs.html" and is created in the current directory or in the same directory as the executable file.<br>
Since URLs Editor tries to read URLs.html existing in the current directory or in the same directory, it is recommended to create and use a shortcut to URLs.html.


### Changing the contents of a bookmark page
When the script is executed, it reads the \<Details\> tag and other structures described in the current directory and URLs.html that exist in the same directory and reflects them in the GUI.<br>
Once you have changed the content as you wish, you can update URLs.html by pressing the button labeled "この内容で反映する".

## What does this script do?
This script appends \<Details\>, \<a href\>, etc. to the predefined CSS styles and javascript in the script and outputs them to a single HTML file.<br>
