# Package Management

Package management is essential for maintaining Linux machines of any distro.
Every distro will have a default package manager installed, others can be installed
as you so wish, however, if you are accessing multiple systems where you may or may not have control over this it is important to understand the different ways of managing packages.

Package managers can be broken down into six key features:

- Package downloading
- Dependency resolution
- A standard binary package format
- Common installation and configuration locations
- Additional system-related configuration and functionality
- Quality control

We can use different package management systems which cover different file types. The package management requirement is that the software to be installed is available as a corresponding package, this is typically created, offered, and maintained centrally under Linux distros.

<br />

___

<details open>
<summary>Commands</summary>

<div align="center">

| Command | Description |
| --- | --- |
| dpkg | The dpkg is a tool to install, build, remove, and manage Debian packages. The primary and more user-friendly front-end for dpkg is aptitude. |
| apt | Apt provides a high-level command-line interface for the package management system. |
| aptitude	| Aptitude is an alternative to apt and is a high-level interface to the package manager. |
| snap	| Install, configure, refresh, and remove snap packages. Snaps enable the secure distribution of the latest apps and utilities for the cloud, servers, desktops, and the internet of things. |
| gem | Gem is the front-end to RubyGems, the standard package manager for Ruby. |
| pip | Pip is a Python package installer recommended for installing Python packages that are not available in the Debian archive. It can work with version control repositories (currently only Git, Mercurial, and Bazaar repositories), logs output extensively, and prevents partial installs by downloading all requirements before starting installation. |
| git | Git is a fast, scalable, distributed revision control system with an unusually rich command set that provides both high-level operations and full access to internals. |
| apt-cache | query the APT cache |q


___

</div>

</details>

<br />

Debian based Linux distributions use the `APT` package manager. A package is an archive file containing multiple `.deb` files. The `dpkg` utility is used to install programs from the associated `deb` file.

Package managers make updating and installing programs easier, as many programs have dependencies. When installing a standalone `deb` file we may run into dependency issues and need to download or install multiple additional packages.

Each Linux distro uses software repositories that are updated often, these are queried when we update a program or install a new one. Repositories can be labelled either as stable, testing, or unstable. Most Linux distributions will utilise the stable version of repositories, usually locatable in `/etc/apt/sources.list` this differs in Parrot however: `/etc/apt/sources.list.d/parrot.list`.

`APT` uses a database known as the `APT cache`. This can be used to discover information about our packages installed on our system offline.

We can list all installed packages using: `apt list --installed`.

<br />

___

<div align="right">

[<< prev](./10_userManagement.md) | [next >>](./)
</div>