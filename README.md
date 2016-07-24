# Vim Basics

## A guide for effectively using vim mode in Visual Studio, Visual Studio Code, or Sublime Text 3

### What is Vim?

Vim is a command-line text editor.
The name stands for "Vi improved" (it is based upon an earlier text editor called Vi).

### What makes Vi(m) special?

Vim is a _modal_ editor (meaning it has difference modes).
Each mode provides a different way of interacting with your text.
With these modes, you can effectively and efficiently manipulate text without leaving your keyboard.

We will focus on three of Vim's modes:
- Insert
- Normal
- Visual

**Insert** mode is most similar to text editors with which you are familiar.
Each key you press (e.g. a, b, \<enter\>, :, #) is inserted directly into the document.

**Normal** mode allows you to move your cursor around the document.

**Visual** mode is for selecting text within the document (to cut or copy).

### Why should I use Vim?

I don't know why (or if) you should use Vim. I can tell you why I use it though.

1. Ease of coding
    - I started using Vim mode because I was tired of jumping from home row to Control+Arrow, Home, and End all the time.
      Vim lets me type without constantly moving around my keyboard.

2. Consistency
    - In the course of one week, I can write code from 4 different keyboards, 3 difference OSes, and 4 different text editors.
      Before using Vim, I would fumble hotkeys when I changed editors or OSes.
      I can go between any combination of keyboard, OS, and editor and have the same experience with Vim.

### Changing modes

- Press `esc` from insert to go to normal mode.


- Press `i` from normal to go to insert before the cursor.
- Press `a` from normal to go to insert after the cursor.
- Press `I` from normal to go to insert at the beginning of the line.
- Press `A` from normal to go to insert at the end of the line.


- Press `v` from normal to go to visual.
- Press `V` from normal to go to visual line (you will select and highlight the entire line).

### Mapping keys

You can map any key (or combination of keys) to anything else.

The only key remap I use is `jk` to `esc`.

Look at the other files in this repository to see how to set up that mapping for your system:

- `.vimrc`: Vim from command line, VSVim extension for Visual Studio, IdeaVim for Jetbrains IDEs
- `Default.sublime-keymap`: Sublime Text 3
- `settings.json`: VSCodeVim extension for Visual Studio Code

Read this for more information about key mapping: http://stackoverflow.com/a/3776182

### Movement (works from normal and visual modes)

#### Basic

- `h`: move left one column
- `j`: move down one line
- `k`: move up one line
- `l`: move right one column

You can visualize it like this:
```
      ^
< h j k l >
    v
```

- `w`: move forward to the beginning of the next word
- `W`: move forward one WORD (similar to a word, but can include things like dashes)
- `b`: move backward to the beginning of the previous word
- `B`: move backward one WORD
- `e`: move forward to the end of the next word
- `E`: move forward to the end of the next WORD
- `0`: move to the first column of the current line
- `^`: move to the first non-whitespace character of the current line
- `$`: move to the end of the line

#### More

- `gg`: move to the beginning of the first line of the document
- `G`: move to the beginning of the last line of the document
- `H`: move to the first visible line on the screen (think High)
- `M`: move to the middle visible line on the screen (think Middle)
- `L`: move to the last visible line on the screen (think Low)

### Helpful things for editing

Deleting and yanking puts the selected contents into a register.
If you do not specify a register, the contents go into the default register.

#### Delete (cut)

- `d<something>`: delete according to `<something>` movement
  - `dw` deletes a word
  - `dG` deletes to the end of the document
  - `dd` is a special case and deletes the current line

#### Copy (yank)

- `y<something>`: copy according to `<something>` movement
  - `yw` yanks a word
  - `yG` yanks to the end of the document
  - `yy` is a special case and deletes the current line

#### Paste

- `p`: paste the default register in front of your cursor
- `P`: paste the default register behind your cursor

#### Undo

- `u`: undo the last action

#### Repeat action

- `.`: repeat the last action (you can move your cursor before repeating the action)

#### Indentation

- `>`: indent the current selection
- `<`: outdent the current selection
- `>>`: indent the current line
- `<<`: outdent the current line
