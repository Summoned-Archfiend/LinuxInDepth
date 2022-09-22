# Processes

Processes are a fundamental part of Linux, as we covered previously we have different types of processes. What we have yet to visit is the states which these processes can be in. We alluded to this previously when we started, stopped, enabled, and disabled `daemons`, which as we know are a type of service themselves.

Any given service can be in a number of states:

- Running - The service is running normally
- Waiting - The service is waiting for an event or system resource
- Stopped - The service is stopped
- Zombie - The service stopped but still has an entry in the process table

Processes can be controlled with various commands we have covered, some aditional commands which can be useful are listed below.

<details open>
<summary>Commands</summary>

<div align="center">

| Command | Description |
| --- | --- |
| kill | Send a signal to a process  |
| pgrep, pkill, pidwait | look up, signal, or wait for processes based on name and other attributes |
| killall | kill processes by name |

</div>

</details>

We can view all the available signals via `kill -l`. Many of these wont make much sense right away, but here are some common signals:

<details open>
<summary>Signals</summary>

<div align="center">

| Signal | Description |
| --- | --- |
| 1 | **SIGHUP** - This is sent to a process when the terminal that controls it is closed. |
| 2 | **SIGINT** - Sent when a user presses **[Ctrl] + C** in the controlling terminal to interrupt a process. |
| 3 | **SIGQUIT** - Sent when a user presses **[Ctrl] + D** to quit. |
| 9 | **SIGKILL** - Immediately kill a process with no clean-up operations. |
| 15 | **SIGTERM** - Program termination. |
| 19 | **SIGSTOP** - Stop the program. It cannot be handled anymore. |
| 20 | **SIGTSTP** - Sent when a user presses **[Ctrl] + Z** to request for a service to suspend. The user can handle it afterward. |

</div>

</details>

We often use these signals when we run process commands, for instance, if I want to force `kill` a process (which you have likely already done before) I would use `SIGNAL` 9, for example: `kill 9 <PID>`.

## Background Processes

Other than killing processes there may be other ways we need to manipulate them. Sometimes it is necessary to put the scan or process we have just started into the background, doing so allows us to free up the terminal session to interact with the system or to start other processes. As we have already seen we can do this with the shortcut **[Ctrl + Z]**, this sends the **SIGTSTP** signal to the `kernel` which suspends the process.

<br />

![Paused Processes](../images/pausedProcesses.png)

<br />

In the above example we start two services, first of all we begin a ping with a count of 10, we interrupt this with a signal to suspend the service via **SIGTSTP**. We then start another service in the same session opening up `vim` to view the contents of `tmpfile`. Since we have suspended these two processes we free up our terminal, but how can we view the services? they haven't stopped running, yet we can no longer see them. This is where the `jobs` command comes in. This command lists all of our active `jobs` (processes) in the session. We can use `bg` to put the process in the background. Another options is to set the process with an ampersand (`&`) at the end of the command, in this case we will see the results when the process finishes.

![Background](../images/background.png)

# Foreground a Process

Using the jobs command we can list all background processes. Backgrounded processes do not require much interaction, and we can use the same shell session without waiting until the process finishes first. Once the scan or processes finishes, we are notified by the terminal. If we wish to pull the background process into the foreground so that we may interacti with it again we can use the forground command `fg`.

<br />

![Foregounrd](../images/foreground.png)

# Executing Multiple Commands

<div align="right">

[<< prev](./13_masking.md.md) | [next >>](./)
</div>