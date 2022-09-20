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
| apt-cache | query the APT cache |
| apt --fix-broken install | Fix unresolved dependencies |

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

At this point we have seen multiple package managers. The main differences are the utilities, for instance, a manager like `npm` or `pip` are for packages specific to a certain language/project (pip for python for example). The difference becomes far less transparent when we look at some of the managers we would more commonly use such as `apt`, `pacman`, `dpkg`. Here the main difference is the repositories the managers fetch from, this means some applications are available on some that aren't on others. For instance, in `arch` if we want to install `vscode` we cannot find this application via `pacman`. We must instead install `yay` (another package manager for the `aur` repository). With `yay` we can then install `vscode` amongst other packages.

Some package managers come with additional features. In the modern era many package managers come with the facilities to search their repositories, to update installed packages, to list installed packages, they automatically resolve dependencies for us making installation a cinch, and sometimes more. If we take `dpkg` for instance, `dpkg` is a low level package manager, it can be useful for installing programs directly from `.deb` files if this is the only method of installation we have access to, however, it is incredibly "dumb". `dpkg` does not have automatic dependency resolution, this means if we are missing dependencies from our installation it will simply `err` and it is up to us to find the packages and resolve the issue. With a more modern manager like `apt` this is not an issue, `apt` will resolve the dependencies for us, this is known as a high level package manager as it is built to be easier for us (the user) to use.

Another type of package manager is stores. A store is exactly the same as other package managers, except, instead of fetching from a central repository, they fetch from an app store. This is similar to the `play` store with google or the `apple` store, these stores are often browsable via a webpage, but we can easily install them via package managers like `snap`.

Lastly, an important note on package managers. When we `remove` an application via package managers like `dpkg` and `apt` this is a "safe" option in which user data is preserved. If instead, we wish to remove all traces of an application we want to run the `purge` command.

___

<div align="right">

[<< prev](./10_userManagement.md) | [next >>](./12_daemons.md)
</div>