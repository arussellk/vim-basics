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

### Basic Movement (works from normal and visual modes)

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

### More Movement

- `gg`: move to the beginning of the first line of the document
- `G`: move to the beginning of the last line of the document
- `H`: move to the first visible line on the screen (think High)
- `M`: move to the middle visible line on the screen (think Middle)
- `L`: move to the last visible line on the screen (think Low)
