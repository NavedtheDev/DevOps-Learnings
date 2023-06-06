* Kernel is the major component of an operating system and is the core interface between a computer's hardware and its processes. It communicates between the two managing resources as efficiently as possible. 

* The Kernel is responsible for four major tasks. 

   1. Memory management : keep track of how much memory is used to store what and where. 
   2. Process management : determine which processes can use the CPU when, and for how long. 
   3. Device drivers : act as a mediator or an interpreter between the hardware and processes. 
   4. System calls and security : receive requests for service from the processes. 
   
* The Linux Kernel is monolithic. This means that the Kernel carries out CPU scheduling, memory management, and several other operations by itself. 

* The Kernel is also modular, which means it can extend its capabilities through the use of dynamically loaded Kernel modules. 

* Let us now look at ways to identify the Linux Kernel version and understand the naming conventions. The Kernel is an integral part of the operating system. Use the uname command to display information about the Kernel. 

```
uname
```

* Use the dash r or dash -a flag to print the Kernel version. 

```
uname -r 
OR 
uname -a
```

* One of the important functions of the Linux Kernel is memory management. Memory is divided into two areas known as Kernel space and userspace. These are synonymous to the terms Kernel and user mode. 

* Kernel space is the portion of memory in which the Kernel executes and provides its services. A process running in the Kernel space has unrestricted access to the hardware. As such, it is strictly reserved for running the Kernel code, Kernel extensions, and most device drivers. 

* On the other hand, all processes running outside the Kernel reside in the user space which has restricted access to CPU and memory. 

* Most Unix-like operating systems, including Linux, come prepackaged with all kinds of utilities programming languages, and graphical tools. These are called user-space applications. This is also often referred to as the Userland. 

* Let us now look at how programs running in the user space work. All user programs function by manipulating data, but where does this data live? Most commonly, it is stored in memory and on disk. User programs get access to data by making special requests to the Kernel called <b>system calls</b>. Examples include allocating memory by using variables or opening a file. For example, opening a file such as the /etc/os-release file to see the version of the operating system installed results in a system call. 















