# User Management

Managing users is an essential part of using Linux. Whether you are a sysadmin, dev, or even just using a personal machine, you will find yourself frequently needing to create users, add them to groups, and manage their permissions. The following will described the basic commands for creating users, you can find more information on these in the ```man``` page, you can also search these commands using ```apropos``` by searching for the user keyword.

When we create users they are saved to, you guessed it, a file, following our Linux philosophy. We can view this file at ```/etc/passwd```.

In viewing this file we see an output as such:

<div align="center">
    <image src="../images/10_useradd.png">
</div>

<br />

In this output we see a lot of data per user. First of all we notice the name of the user, we will focus on the final user ```thor```. Here we see most of our users are superseded by an ```x```. This ```x``` indicates to use that this user has a ```password``` set in another file known as the ```shadow file```. 

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