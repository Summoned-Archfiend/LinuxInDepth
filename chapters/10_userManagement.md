# User Management

Managing users is an essential part of using Linux. Whether you are a sysadmin, dev, or even just using a personal machine, you will find yourself frequently needing to create users, add them to groups, and manage their permissions. The following will described the basic commands for creating users, you can find more information on these in the ```man``` page, you can also search these commands using ```apropos``` by searching for the user keyword.

When we create users they are saved to, you guessed it, a file, following our Linux philosophy. We can view this file at ```/etc/passwd```.

In viewing this file we see an output as such:

<div align="center">
    <image src="../images/10_useradd.png">
</div>

<br />

In this output we see a lot of data per user. First of all we notice the name of the user, we will focus on the final user ```thor```. Here we see most of our users are superseded by an ```x```. This ```x``` indicates to use that this user has a ```password``` set in another file known as the ```shadow file```, this is located within the ``etc`` directory under ``shadow``. If we cat this file we can see a list of yet more information, but we should be able to also see any user we created. For me this is ``Thor``, next to the user you should be able to see a hashed version of their ``password``.

Next to the ``x`` in our ```passwd``` file, you see two numbers. In the above image it is ```1001/1004``` this is the ```User ID (UID)``` and ```Group ID (GID)```. Notice that all we did here was create a user, yet Linux created both a user and a group of the same name.

At the end of here, after the username, we see the ``home`` directory for the user, and finally at the very end of the line we have the users default ```SHELL```, in ``Thors`` case this is ```BASH```.

We have two means of adding users, ```addUser``` which we have already touched and ```userAdd```. When we run ```addUser``` we get a longer prompt for additional setup, however, if we do the same with ```userAdd``` you will instantly notice this missing, that the user is simply just created. This command is lazy and does the bare minimum, this means we have to set up any additional information ourselves, including setting our passwords and even home directory. We would also notice a difference in default ``shell``, this method of creating a user tends to default the shell to ``sh`` rather than ``bash``.

We can amend users using `usermod`. As such, we can modify any details in the `passwd` file, for instance, we can change the shell tht we use by default:

<pre>
<code>
sudo usermod username --shell /bin/bash
</code>
</pre>

We can also impersonate other users temporarily. This is done via the `su` command, running it allows us to switch users. We run this command with `su - username`, if we fail to provide a username this command will default to the `root` user. We will of course be required to provide the password for the user we switch to, unless we use the `sudo` command. Sudo gives us ultimate power, it enables us to temporarily act as the `root` user, we never want to actually login as the `root` user because the power it gives us is dangerous, especially so in the wrong hands, if we ran a malicious script as `root` it could `pwn` our entire system easily, but using sudo we can access other users. If you try changing to another user, and attempt to use their account to create another user, you will notice you receive a warning. This is because the user just created has no permissions, even attempting to use `sudo` you will find a warning, this occurs due to the lack of an entry in the `sudoers` file.

We can edit the `sudoers` file to add an entry for our newly created user, after all just like everything in Linux it is a `file`, however, we must be more careful in doing so with the sudoers file, as messing up the sudoers file can destroy your entire system if not careful. As such, we cannot simply add an entry using `vi` or `vim` like we normally would, we must instead use `sudo visudo`, we use this as it is the only "safe" method of editing the sudoers file. Unlike our regular text editors `visudo` edits the sudoers files in a manner analogous to `vipw`. The sudoers file is locked against multiple simultaneous edits, it also performs basic validity checks, If the `sudoers` file is currently being edited you will be prompted to try again later. But it doesn't stop here, `visudo` then runs checks after editing, it parses the `sudoers` file and will not save the changes if there are syntax errors, Upon finding an error a message will appear with the line number of where the error occurred.

<br />

<details open>
<summary>Commands</summary>

<div align="center">

| Command | Description |
| --- | --- |
| adduser | add a user or group to the system |
| useradd | create a new user or update default new user information |
| usermod | modify a user account |
| su | run a command with substitute user and group ID |
| visudo | edit the sudoers file |

</div>

</details>

___

<div align="right">

[<< prev](./4_parrot.md) | [next >>](./6_filesystemRoot.md)
</div>