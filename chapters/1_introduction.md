# Introduction To Linux

Linux is a computer Operating System (OS) created in the 90's by a the Finnish engineer [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds). An OS is system software that manages computer hardware interaction, system resources, and provides common services for computer programs.

The OS is initially loaded into computer memory by a boot program, the OS manages all other application programs on a computer by allowing application programs to make use of it by making requests for services through a defined Application Programming Interface (API). This allows users to interact directly with the OS through a User Interface (UI), this can be a Graphical User Interface (GUI) or a Command Line interface (CLI).

An OS brings powerful benefits to the use and development of computer software. Without an OS, every application would need to include it's own UI, as well as comprehensive code necessary for handling all low-level functionality of the underlying computer, this would have to include processes such as disk storage, network interfaces, hardware interactions, and everything else...

This would be highly problematic for engineers developing software as the hardware of each individual machine may change considerably. This would also vastly increase the size of every application and make developing new software highly impractical.

Rather than doing this overly-complex approach, which also breaks the tenets of programming (keeping it DRY for example), many of the common tasks, such as sending network packets, displaying text, etc... can be offloaded to system software that serves as an intermediary between applications and hardware. The system software provides a consistent and repeatable way for applications to interact with hardware without the applications needing to know any details of the hardware.

Using this approach, so long as each application accesses the same resources and services in the same manner as the system software, the OS is able to service an arbitrary number of applications This reduces the amount of time required to develop and debug an application, whilst still ensuring that users can control, configure and manage their system hardware through a common UI.

Once installed the OS relies on a vastly large library of device drivers. These tailor the OS services to the specific hardware environment. This means that every application may make a common call to, for example, a storage device, but it is the OS which receives that call, the OS will then use the corresponding driver to translate that call into actions necessary for the underlying hardware on that specific computer.

In modern computers, the OS provides a comprehensive platform itself, that identifies, configures, and manages, a range of hardware including; processors, memory devics, and memory management, chipsets, storage, networking, port communication, memory devices, memory management, VGA, HDMI, USB, and subsystem interfaces such as PCIe.

An OS provides three essential capabilities:

1. A UI - offered through CLI or GUI - launches and manages application execution as well as identifies and exposes system hardware resources to those applications via a standard API.
2. Application Management - An OS must handle the launch and management of every application. Typically supports an array of behvaiours including threads to enable processes to share access to processors. The OS may also support APIs which enable applications to utilise OS hardware functions without needing to know anything about the low-level OS or ahrdware state.
3. Device Management - An OS is responsible for identifying, configuring, and providing applications with common access to hardware devices.

<div align="center">

![OS](../images/OS.png)

</div>

Linux itself is a general purpose OS. This means that Linux is an OS like Windows, or macOS, which manages all of the hardware resources associated with a computer. Throughout this guide I will be using a PwnBox known as ParrotOS via [hackTheBox](https://academy.hackthebox.com/).


___

<div align="right">

[<< prev](../README.md) | [next >>](./2_phillosophy.md)
</div>
