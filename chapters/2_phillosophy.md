# Philosophy of Linux

Linux follows a simplistic Philosophy consisting of five core principles. We can also break the Linux OS down into layers to make it easier to understand communication between each layer.
 ___

<details open>
<summary>Philosophy</summary>

1. Everything is a file - all configuration files for the various running services on the Linux OS are stored in one or more text files.
2. Small, single-purpose programs - Linux offers many different tools that we will work with, which can be combined to work together.
3. Ability to chain programs together to perform complex tasks - The integration and combination of different tools enable us to carry out many large and complex tasks, such as processing or filtering specific data results.
4. Avoid captive user interfaces - Linux is designed to work mainly with the shell (or terminal), which gives the user greater control over the operating system.
5. Configuration data stored in a text file - An example of such a file is the /etc/passwd file, which stores all users registered on the system.

</details>

___

<details open>
<summary>Components</summary>

| Component | Description |
| --- | --- |
|Bootloader | A piece of code that runs to guide the booting process to start the operating system. Parrot Linux uses the GRUB Bootloader. |
| OS Kernel | The kernel is the main component of an operating system. It manages the resources for system's I/O devices at the hardware level. |
| Daemons | Background services are called "daemons" in Linux. Their purpose is to ensure that key functions such as scheduling, printing, and multimedia are working correctly. These small programs load after we booted or log into the computer. |
| OS Shell | The operating system shell or the command language interpreter (also known as the command line) is the interface between the OS and the user. This interface allows the user to tell the OS what to do. The most commonly used shells are Bash, Tcsh/Csh, Ksh, Zsh, and Fish. |
| Graphics server | This provides a graphical sub-system (server) called "X" or "X-server" that allows graphical programs to run locally or remotely on the X-windowing system. |
| Window Manager | Also known as a graphical user interface (GUI). There are many options, including GNOME, KDE, MATE, Unity, and Cinnamon. A desktop environment usually has several applications, including file and web browsers. These allow the user to access and manage the essential and frequently accessed features and services of an operating system. |
| Utilities | Applications or utilities are programs that perform particular functions for the user or another program. |

</details>

___

<details open>
<summary>Linux Architecture</summary>

| Layer | Description |
| --- | --- |
| Hardware | Peripheral devices such as the system's RAM, hard drive, CPU, and others. |
| Kernel | The core of the Linux operating system whose function is to virtualize and control common computer hardware resources like CPU, allocated memory, accessed data, and others. The kernel gives each process its own virtual resources and prevents/mitigates conflicts between different processes. |
| Shell | A command-line interface (CLI), also known as a shell that a user can enter commands into to execute the kernel's functions. |
| System Utility | Makes available to the user all of the operating system's functionality. |

</details>

___

## Communication

![OS Communication](../images/OS.png);


<div align="right">

[<< prev](./1_introduction.md) | [next >>](./)
</div>
