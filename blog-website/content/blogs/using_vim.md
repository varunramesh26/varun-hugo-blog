---
title: "Using Vim Editor"
#date: 2022-01-27T11:39:08+05:30
draft: false

# weight: 1
# aliases: ["/vim"]
tags: ["editors","vim"]
author: "Me"
# author: ["Me", "You"] # multiple authors
description: "Intro to Vim Editor"

showToc: true
TocOpen: false
hidemeta: false
comments: false
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/varunramesh26/varun-hugo-blog/blog-website/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---


## Text Editors and IDEs

Text editors are applications that are used to write the source code. It comes with an user interface to write the code in it, and save it back at a location specified.

**Ex:** *Vim, Neovim, Emacs, Nano, Sublime-Text, Notepad++, Brackets etc.,*

Integrated Development Environment (IDE) provides multiple tools like a text editor to write the source code, build automation tools to compile or build the program written, source code execution tool, debugger to inspect the errors, and many more features.

**Ex:** *Visual Studio IDE, Visual Studio Code, Geany, Netbeans, Eclipse, IntelliJ, Pycharm, RStudio, etc.,*

Some of the text editors like *Vim* or *Sublime* can be extended to use it like an IDE, which will be much more lightweight on the system resources.

---

## Using VIM

VIM is an improved version of Vi text editor, highly configurable which makes the workflow efficient. To open a VIM instance enter **vim** at the prompt("$" or "#") in a terminal (assuming that VIM is installed on your system).

### Installing & Verifying VIM
To install **VIM** on *Ubuntu* or *Ubuntu* based distros (operating systems) like *Mint*, or *Windows Subsystem for Linux*, please use the following command:

```terminal
$sudo apt-get install vim
```

More on **apt-get** [click here](http://manpages.ubuntu.com/manpages/xenial/man8/apt-get.8.html), or go to **man apt-get** through terminal.

To install **VIM** on *Arch Linux* based distros (operating systems) like *Manjaro*, use the following command:

```terminal
$sudo pacman -S vim
```

More about pacman [click here](https://www.archlinux.org/pacman/pacman.8.html), or go to **man pacman** through the terminal.

To verify **VIM** installation:
```terminal
$vim
```

### How to Navigate in VIM.
To move around in VIM, across the lines, or from left to right, or vice versa use the following keys in the **NORMAL** mode.

- **j** - down
- **k** - up
- **h** - left
- **l** - right

Similar to the arrow keys:

![VIM-Navigation](/using_vim/vim-navigation.png)

### Four Major VIM modes:

- Normal Mode
- Insert Mode
- Visual Mode
- Replace Mode

1. **Normal Mode:**
In this mode we can use VIM editor commands by pressing **":"**. One can move around the editor while being in this mode.

2. **Insert Mode:**
To get into insert mode press **i** in Normal Mode, and *--INSERT--* will be displayed at the bottom of the editor. Only through this mode a user can write the something in VIM. To quit out of the insert mode press **"ESC"** key.

    ![Insert Mode](/using_vim/insert-mode.png)

3. **Visual Mode:**
This mode is used to highlight an area of code, which can be later copied or modified. To use this mode press **"v"** while in Normal mode, and it dispays *--VISUAL--* at the bottom.
Visual line mode highlights the lines, press **"SHIFT+V"**. It displays *--VISUAL LINE--* at the bottom.
Visual block mode highlights blockwise, press **"CTRL+V"**. It displays *--VISUAL BLOCK--*.

    ![Visual Mode](/using_vim/visual-mode.png)

4. **Replace Mode:**
This is a special kind of insert mode, where it deletes the characters under the cursor, and replaces whatever we enter. To enter into replace mode press **"SHIFT+R"**. It displays *--REPLACE--* at the bottom of the editor.

    ![Replace Mode](/using_vim/replace-mode.png)

**NOTE:** To exit any mode and return to NORMAL mode press **"ESC"**.

5. **Command-Line Mode:**
This is where one enters the commands. To enter this mode simply press **colon(:)**.

    ![Command Mode](/using_vim/cmd-mode.png)

- **:w** - saves the appended text or modified text into the file
- **:q** - quits the VIM text editor
- **:q!** - discards the changes made, and quits the VIM text editor
- **:wq** - saves the changes and quits the VIM text editor
- **:50** - jumps to the specified line number i.e. 50 here
- **:his** - lists out the history of commands that was used previously

#### Search Pattern and Replace Commands:

- **/search-pattern** - searches for the pattern passed after **"/"**
- **:%s/search-pattern/replacement** - searches for the *search-pattern*, and replaces all the instances of it with *replacement* string.
- **:%s/search-pattern/replacement/gc** - matches the *search-pattern*, starts replacing it with a *replacement* pattern, and asks for confirmation at every instance of the search-pattern found.

#### Operators:
The operators are used to manipulate the code or the text. Use these commands in **NORMAL mode**.
- **d** - delete the highlighed area
- **y** - yank or copy the highlighted area
- **p** - paste the last deleted area or the yanked code after the cursor
- **r** - replace a character under the cursor
- **u** - undo the last modification

#### Motion Operators:
It **provides context to the operators**, or the cursor jumps multiple words or to the EOF. These can be combined with the above operators.
- **w** - jumps to the first character or the start of next word
- **e** - jumps to the last character or the ending of next word
- **b** - jumps to the beginning of previous word
- **$** - jumps to the end of line
- **0** - jumps to the beginning of a line
- **gg** - jumps to the beginning of the file
- **G** - jumps to the end of the file
- **}** - jumps to beginning of next paragraph
- **{** - jumps to end of the paragraph

**Deleting a word:**
- **dw** - deletes a word starting from the cursor until the next word
- **de** - deletes a word starting from the cursor until the end of the word
- **d5w** - deletes 5 words starting from the cursor
- **d4b** - deletes 4 previous words starting from the cursor
- **d$** - deletes the words from the cursor until the line ends
- **d3$** - deletes 3 lines after the cursor position.

#### Search & Highlight Patterns
- **/word_to_be_highlighted** - highlights all the words or patterns matching *word_to_be_highlighted* string
- **n** - to move to the next search match
- **N** - to move to the previous search match
- **:noh** - is used to clear the last search pattern highlighting

    **NOTE:** For further help use **":help"** command in VIM, it brings up the manual for VIM.

    ![VIM Help](/using_vim/vim-help.png)

    ![Help page](/using_vim/help-page.png)

- For practicing how to use VIM, please refer to the **vimtutor** section in the VIM manual.
    In the above page, place your cursor on **vimtutor** highlighted in blue color, and then press **CTRL+]**, which opens up the vim tutorial:

    ![VIM Tutorial](/using_vim/vim-tutor.png)

    Follow the instructions, and learn how to use VIM effectively.

---


