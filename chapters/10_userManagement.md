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

<br />

<details open>
<summary>Commands</summary>

<div align="center">

| Command | Description |
| --- | --- |
| adduser | add a user or group to the system |
| useradd | create a new user or update default new user information |
| | |

</div>

</details>

___

<div align="right">

[<< prev](./4_parrot.md) | [next >>](./6_filesystemRoot.md)
</div>