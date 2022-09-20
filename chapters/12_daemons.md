# Daemons

Daemons are internal services, these include, the relevant services required at system startup (e.g. these perform hardware-related tasks, services installed by the user, server services etc...). These services run in the background without the need for user interaction. These services are known as `Daemons` and are identifiable by the letter `d` at the end of the program name: `sshd`, `systemd`.

Most Linux distros have switched to `systemd` as their `daemon` for the initialisation process. This `daemon` is the first to start, and thus has the `PID` of `1`. The job of this `daemon` is to monitor and take care of the orderly starting and stopping of other services. All processes have an assigned `PID`, viewable under the `/proc/` filepath with their corresponding `PID` number. Any one of these processes may also have a parent process (`PPID`). A process is considered to be anything which is an instance of a running program.

The term `Daemon` originates in Greek Mythology as a supernatural being which interferes, or performs tasks, from behind the scenes. When we deal with `Daemons` we will need to deal with  a process known as the `Master Daemon`. The master `Daemon` is `systemd`, this `Daemon` is the commander of all other `Daemons`. `Systemd` starts the `Daemons`, stops the `Daemons`, restarts the `Daemons` and more. Practically anything we want to do with `Daemons` has to go through `Systemd`.

`Systemd` has two main roles. First of all, `Systemd` is a service manager. Second, the `Systemd` acts as the initialisation system, this is vital to the boot process. When we boot our system we fire up the boot process, this in turn loads the system kernel, the kernel then hands over to `Systemd` who then continues tasks such as mounting the filesystem, starting the `Daemons` etc...

From `Systemd` a process called `forking` starts the other `Daemons` with their own `PIDs`. We can view running `Daemons` using `systemctl`, we can lsit processes with `ps -aux`, and we can even see a tree of processes starting via `pstree`.

While many Linux distros have standardised to use `Systemd` as the master `Daemon`, there are other initialisation systems available, older distros and systems can have other init systems such as; `sysvinit`, `upstart`, and `openrc`. When we use `Systemd` we need to knwo that `Systemd` itself does not refer to other `Daemons` as `Daemons`, but as `units`.

<details open>
<summary>Commands</summary>

<div align="center">

| Command | Description |
| --- | --- |
| systemctl | Control the systemd system and service manager |
| systemctl stop `service` | stop a running `daemon` or `service` |
| systemctl status `service` | status of a `service` or `daemon` |
| systemctl start `service` | start a `daemon` or `service`|
| systemctl restart `service` | restart a `daemon` or `service` |
 systemtl reload `daemon` | reload a configuration, not every `service` or `daemon` can do this |
 | systemctl reload-or-restart `service` | reload a `service` if possible, otherwise just `restart` |

</div>

</details>

<br />

___

<div align="right">

[<< prev](./11_packageManagement.md) | [next >>](./12_daemons.md)
</div>