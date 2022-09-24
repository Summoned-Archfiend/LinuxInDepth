# Editing Files

There are several ways to edit files in Linux. One of my personally favored ways is `vim` or `vi`, either one of both of these are usually installed on a system, `vi` is older, `vi` itself actually stands for `visual` as an early text editor, it preceded the early implementation of `ex` (Extended) which was a line editor back when computers were merely printing terminals rather than actual screens. In `ex` people worked with line numbers, editing individual lines as necessary.

`Vim` on the other hand, stands of "Visual IMproved", it is an early implementation of the `vi` standard but with many additions. Most distros will have `vim` preinstalled. We will not go into too much details on the history of this but Shell Tips has a great article on the matter [here](https://www.shell-tips.com/linux/vi-vs-vim/#gsc.tab=0) if that is a rabbit hole you would like to dive down.

Other options for editing files are `nano`, which I know is highly loved by many I have worked with, however, once you are used to `vim` it becomes just as easy to use. You often need to install `nano` separately however as it is not covered under the `GPL` liscence, meaning it is not included in distros as default, though neither is `vim` if you use `DIY` OS like `Arch`. Nano does offer some nice quality of life improvements, such as opening multiple files, per line scrolling, etc. You can choose whatever text editor you prefer, but there is always a trade off, for instance, `nano` may be easier to use, but `vi` is more powerful and provides macro programming commands which can help increase your productivity. A trick I use many of the time in work is to use `VSCode`, if you `SSH` to a remote server using the `remote` extension you can actually open any file on the server in your `VSCode` via the command `code <PATH>` (it is often surprising how many devs don't know about this!).

Here I will focus on `vim` nano is particularly easy to use, much of the same rules apply generally across text editors, but by learning `vim` you will have a greater starting point across various text editors, even for going further back into `vi` if you so wish. If we want to create a new file in `vim`, or even edit an existing file, we need only use the command `vim <PATH>` where we pass either the path to an existent text file, or to a new text file that `vim` will create for us.

In doing so you will be met with a editor page, you will notice that you are unable to type within this editor right away. This is because vim has three modes `Normal`, `Insert`, and `Visual`.

<details open>
<summary>VIM Modes</summary>

___

## Normal

We begin in `Normal` mode, in this mode you are totally unable to insert any character what so ever. This is also known as command mode because any keystroke you enter will be interpreted as a `command`, for instance pressing `K` will move the cursor position up one line, similarly `yy` will copy the current line, `gg"+yG` would yank from the whole file to the clipboard, this is essentially copying the whole file, which can then be pasted with `"+p`, pressing `o` will create a new line for text above the current cursor location. `Normal` mode is necessary for saving out files, or quitting `vim`.

<details>
<summary>Commands</summary>

| Command | Description |
| --- | --- |
| :w | write file to the disk |
| :q | quit without saving |
| :wq | write file to disk and quit |
| :q! | ignore warning and discard the change |
| :w filename | save the file as filename |
| :help | show help for VIM |
| j | move the cursor down one line |
| k | move the cursor position up one line |
| l | move the cursor to the bottom of the screen |
| 0 | move the cursor to the beginning of the line |
| $ | move the cursor to the end of the line |
| I | insert text at the beginning of the line |
| i | insert text before the current cursor location |
| a | insert text after the cursor location |
| o | create a new line for the text below the current cursor location |
| O | create a new line for text above current cursor location |
| CC | remove the whole line and start insert mode |
| s | remove the character under the cursor and start insert mode |
| r | replace the character under the cursor |
| y | copy the selected text to clipboard |
| yy | copy the current line |
| p | insert the text before the cursor |
| P | inert the text after the cursor |
| X | delete the character before the cursor |
| x | delete the character under the cursor |
| D | cut to the end of the line |
| dd | cut the current line |
| u | undo last change |
| Ctrl + R | redo |

</details>

___

## Insert

Insert mode is where we are able to actually enter our text into a file, in this mode every character we type inserts at the cursor location. To enter `insert` mode we press `i` from `normal` mode, we can then enter our text, we can exit back to normal mode via the escape key `ESC`, at which point we can use the commands `:wq` to write and quit or `:q!` to simply quit, with other commands available too.

___

## Visual

In visual mode we can select text to perform operations such as cut, copy, paste, &delete. To switch to visual mode we can enter `v`, `V`, `SHIFT + V`, or `CTRL + v` from `normal` mode.


</details>

For learning `Nano` in more detail I would highly recommend making an account with [HackTheBox](https://academy.hackthebox.com/module/18/section/93) and taking on their free [Linux Fundamentals](https://academy.hackthebox.com/module/18/section/93) course, since I haven't use it much myself I do not actually recall it's usage well. A useful integration with `vim` is `vimtutor`, a command which will open up a practice terminal which will guide you through using `vim`.

<br />

___

<div align="right">

[<< prev](./16_navigation.md) | [next >>]()
</div>