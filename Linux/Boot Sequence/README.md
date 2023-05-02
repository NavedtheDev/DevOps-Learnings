* The boot process can be broken down into four stages:

   1. BIOS POST
   2. boot loader or the GRUB2
   3. kernel initialization
   4. service initialization using systemd 
   
1. The first step called BIOS POST has very little to do with Linux itself. POST stands for power-on self-test. In this stage, BIOS runs a POST test to ensure that the   hardware components attached to the device are functioning correctly. If POST fails, the computer may not be operable and the system will not proceed to the second stage of the boot process. 

2. The next stage after POST is the boot loader. After a successful POST test, the BIOS loads and executes the boot code from the boot device, which is located in the first sector of the hard disk. In Linux, this is located in the /Boot File System. The boot loader provides the user with the boot screen often with multiple options to boot into such as Microsoft Windows OS or an Ubuntu 18.04 OS, in an example of a dual boot system. Once the selection is made at the boot screen, the boot loader loads the kernel into memory, supplies it with some perimeters, and hands over the control to the kernel. A popular example of the boot loader is the GRUB2, which stands for Grand Unified Bootloader version 2, and it is now the primary boot loader for most current Linux distributions. After the selected kernel is loaded into the memory, it is usually decompressed. This is done as the kernels are generally in a compressed state to conserve space.  

3. The kernel is then loaded into the memory and starts executing. During this phase, the kernel carries out tasks such as initializing hardware and memory management tasks among other things. Once it is completely operational, the kernel looks for an init process to run, which sets up the user space and the processes needed for the user environment. 

4. In most of the current day Linux distributions, the init function then calls the systemd daemon. The systemd is responsible for bringing the Linux host to a usable state. Systemd is responsible for mounting file systems, starting and managing system services. Systemd is the universal standard these days 
