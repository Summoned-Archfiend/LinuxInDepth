# FileSystem Root

The first thing we will discuss when talking about Linux is the Root of the filesystem.
If we list the directories at the Root location of Parrot we see a large list of directories and files of varying names which can appear a little intimidating at first (though we have actually covered these locations in previous chapters already). This is the idea we were talking about in the Philosophy section, in Linux systems, everything (literally) is a file; configuration, network settings, IP, profiles, devices, are all represented as files in Linux, even the commands we use are represented by files.

![Parrot Root](../images/parrotRoot.png)

If we enter our bin (binaries) directory we can quickly see that our commands are listed within the directory (note that in the example I have filtered to a specific command, this is because there are so many it is difficult to display, just take a look yourself!). The bin folder contains our essential command binaries. If we ```cat```, standing for concatenate, one of these files we can view the content of these commands. You will see the command binary printed on the screen, this is not human-readable, instead it is a binary string of which the layout is specified by formatString.

![Parrot Bin](../images/binFiles.png)

So, we now understand where our command binaries are stored in Linux, however, heading back to our root directory you may notice another directory named ```sbin```. Much like the ```bin``` folder this directory contains commands, however, these are commands that are required to boot the system which are not executed by normal users. In this sense, it can be useful to think of this as the ```super bin```. Lets enter the ```sbin``` directory to demonstrate what is meant by this.

![Parrot Sbin](../images/sbin.png)

Looking down here you should see a list of commands, note again that they are files following our Linux philosophy. These commands are special, in the sense that they are only usable by administrators.

If you want a hands on example of the types of commands, try running ```sudo adduser``` and create a new user for yourself. If you cannot see this command in the directory as it is you can always pipe the ```grep``` command to search for a specific string on your ```ls```. Once you have created a user cd back to our root directory, take note of the ```usr``` directory within root.

If you list the contents of the usr directory you may find a bit of a shock. If you have never accessed this directory before it can be somewhat confusing, notice how there is yet another ```bin``` and ```sbin``` directory within our ```usr```, see if you can work out what this directory is for before continuing reading. If you list the contents of these directories you will see much the same that we saw in the previous two directories we examined. If you are interested in knowing about the history of this there is an interesting rationale as posted by a user on the [askUbuntu forums](https://askubuntu.com/questions/130186/what-is-the-rationale-for-the-usr-directory).

![Root Usr](../images/usr.png)

Moving on, the usr/bin and usr/sbin directories are essentially the same as the bin and sbin directories, however, the usr/bin and usr/sbin will typically house more commands. Now you may be wondering: "if these commands are in multiple locations, how do we know which one we are using? am I running the usr/bin/ls or the bin/ls?" we can check the path of the command using ```which```.

![Which Command](../images/which.png)

Notice that in either location we use the same ```ls``` command from the ```usr/bin``` directory. 