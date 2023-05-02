* Kernel is the major component of an operating system and is the core interface between a computer's hardware and its processes. It communicates between the two managing resources as efficiently as possible. 

* The Kernel is responsible for four major tasks. 

   1. Memory management : keep track of how much memory is used to store what and where. 
   2. Process management : determine which processes can use the CPU when, and for how long. 
   3. Device drivers : act as a mediator or an interpreter between the hardware and processes. 
   4. System calls and security : receive requests for service from the processes. 
   
* The Linux Kernel is monolithic. This means that the Kernel carries out CPU scheduling, memory management, and several other operations by itself. 

* The Kernel is also modular, which means it can extend its capabilities through the use of dynamically loaded Kernel modules. 

* Let us now look at ways to identify the Linux Kernel version and understand the naming conventions. The Kernel is an integral part of the operating system. Use the Uname command to display information about the Kernel. 

```
uname
```
