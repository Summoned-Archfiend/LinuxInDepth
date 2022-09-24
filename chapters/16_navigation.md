# Navigating Linux

The best way to learn Linux is, like most things, to get hands on with it, to dive into it, and to keep diving into it. The more you do with Linux the more it will become second nature. For example, I dabbled in Linux for a long while, jumping in and out of it, for a full year at University I forced myself to use `Ubuntu` but found it wasn't to my liking. Then, I dabbled in other `distros`, only when I started to use a `Linux` console on a regular basis did I really begin understanding what each part of the system is for, how it works, how it can be manipulated, and what I can do with it overall. The lesson to be learned from this:

<br />

<pre>
<em>"for something to become second nature it is not enough to simply use it regularly, you must immerse yourself in it entirely, even if only for a short while."</em>
</pre>

<br />

You did not learn to talk only by doing so once in a while, you were immersed in an environment with other humans talking to you constantly, you did not learn to read or write by only doing so when you felt like it, you were made to sit and read, or write, you possibly even hated being made to do so at the time, yet now it is not only evident, but undeniable, that you have benefited greatly from such discipline, without it you would not be reading this right now.

So, how can you translate this lesson into learning a new `OS`? or any skill for that matter? you can `immerse` yourself in the realm of the knowledge you wish to attain. In regards to Linux this means to switch your primary `OS`, force yourself to go through the hardship day to day of completing tasks using it, it will be slow and frustrating to start, but you will be all the better for it. As I said, I personally found I did not like `Ubuntu`, I am not even entirely sure why, maybe it was that the `GUI` was not to my liking, even after customising parts, and switching out others, maybe it was that the system itself contained bloatware I never intended to use, and  I very much dislike having a messy system, or maybe it is simply my sub-concious desire to break away from the usual and normative technologies, I don't even know myself truly!

What I do know is, I fell in love with `Arch` from th moment I first used it. Using `Arch` felt right, although it required a lot of configuration I enjoyed the control it gave me over my system. If you wish to learn more about `Arch` I will link my document on it [here](TODO) once it is publicly available.

When we navigate Linux systems we have a few basic commands which we have already come across previously. It is of foremost important that we know: 1. where we are in the system, how can we navigate if we don't know where we currently stand? the answer is we can't, not with any accuracy, and 2. who we are, this determines what permissions we have as a user. To find `where` we are we can use the `pwd` command (print working directory), this will print the current path from our `root` to our current directory. Next, we need to know where we can go, what directories can we enter? we could `cd` into a directory blindly and hope it exists, maybe you do this often with tab completion, but you will also need to `see` your system, this is where `ls` comes in, think of this as the `list` command, which will list all files and directories in the current directory you are in, or in the path you provide should you pass an argument, furthermore we can list even hidden files if we pass a few `switches` namely `-al` (or as I call it the `all` flag), realistically the 'a' shows all of our files, the `l` tells the console we want to see the `long` format, however, if like me you find it useful to remember by assigning words to commands there is no harm so long as you remember that these are two separate flags with different intentions, you can always check the exact definitions in the `man`ual.

When writing console commands remember, the console is your friend, it is there to give you a hand when interacting with the `kernel`, as such, tab completion can be incredibly useful, try typing `cd` and pressing `tab` twice. You will notice that the console outputs a useful list of potential targets for the command. Now, try typing `sys` and doing the same. You will see a list of suggested commands, this can be useful if you cannot recall the exact name of a command. Now do the same but with `systemc` you will notice the command automatically completes, this occurs when a command has enough characters to be uniquely identifiable by the `kernel`, it can work with `paths` too, along with `docker` container names.

Another way we can list commands is using `compgen`, with a number of switches we can list all of the commands we have access to (`-c`), all of the aliases (`-a`), all of the built-ins (`-b`), keywords (`-k`), functions (`-A`). We can even combine the above into a single command `compgen -A -abck`, remember we can also search these lists using a general regex expression (`grep`).

Thus far we have covered the main `Navigatoinal` tools of linux, this is mostly for getting around the filesystem, however, it is also important to know how to create, edit, move, and remove files and directories. The `touch` command for instance allows us to create new files, the same command for directories is `mkdir`. Touch can be a difficult one for newcomers to remember, `mkdir` however is relatively easy (Make Directory).

If we want to move a file, we can do so using `mv` (move), we can also move a directory with this command. We can even move directories and their contents making this a powerful, but potentially dangerous, command. We can copy files and directories using `cp` but may need to do so recursively if we have a directory of multiple files `-r`.  We can check our filesystem tree using the `tree` command.

Try out different switches from the `man` file, for instance, if we use `ls` we can order the output using `-ltc` to show us the files by the order of last created, this can be useful if we want to find the file last changed, or if we are seeking a specific backup date. It is important to practice all of these commands, more so,
to actually read through the `man` pages and learn to understand their layout, they will often tell you exactly how to use the command if you know how to read it, but even that can take practice. My Advice, try them out, use a containerised environment as to build confidence, run each command, set yourself a goal and try to replicate that state with the commands, the more you use them, the better, if you work on Linux systems this is where you will have the advantage using these commands day-in-day-out will help cement your knowledge, you can even take up writing about it, don't worry about getting the details perfect, just about getting your thoughts down, in this way you cement your knowledge in long term memory, and who knows, possibly help someone else who is on the same journey after you.

<br />

___

<div style="font-size: .7em">

If it isn't obvious, the best way to understand these commands is to check the `man` entry, <br /> but also to try these out as you read through.


</div>

___

<div align="right">

[<< prev](./15_webservices.md) | [next >>](./17_editingfiles.md)
</div>