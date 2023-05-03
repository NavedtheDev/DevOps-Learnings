* Let us first understand what a package is. A package, in its simplest definition, is a compressed archive that contains all the files that are required by a particular software to run. 

* A package manager is a software in a Linux system that provides a consistent and automated process of installing, upgrading, configuring, and removing packages from the operating system. 

* Some of the essential functions of a package manager are:

   1. Ensuring the integrity and authenticity of the package by verifying their digital certificates and checksums. This is to ensure that the package is downloaded from  a trusted source and safe to install. 
   2. Simplifying the entire package management process, most package managers provide powerful querying options, making it easier to look up packages and then downloading, installing, or updating existing software.
   3. Grouping packages by function to reduce user confusion. 
   4. Managing dependencies to ensure a package is installed with all packages it requires, thus avoiding what is commonly known as dependency hell.



* Depending upon the distribution, a Linux system supports several different types of package managers. Some of the common ones are:

   1. dpkg, the base package manager for Debian-based distributions
   2. apt, a newer front end for the dpkg system found in Debian-based distributions such as Ubuntu, Linux Mint, and Elementary OS. 
   3. Apt-get is the traditional front-end for the dpkg system found in Debian-based distributions. 
   4. RPM, the base package manager found in Red Hat-based distributions such as Red Hat Enterprise Linux, CentOS, and Fedora. 
   5. YUM, a front-end for the RPM system found in Red Hat-based distributions. 
   6. DNF, a more feature-rich front-end for the RPM system. 



## RPM ##

* It stands for Red Hat Package Manager. This package manager is used in Red Hat Enterprise Linux, as well as other Linux distributions, such as CentOS and many versions of Fedora.
* The file extension for packages managed by RPM is .rpm. 
* Let's see how to work with RPM using the Linux command line. RPM has five basic modes of operation: 

   1. installing
   2. uninstalling
   3. upgrade 
   4. query 
   5. verifying

* Each of these modes can be run using the RPM command followed by specific command options. 



## YUM ##

* YUM stands for Yellowdog Updater Modified, and it is a free and open-source package manager that works on RPM-based Linux systems. 
* YUM works with software repositories, which are essentially a collection of packages, and provides package and dependency management on RPM-based distros. 
* The repository information is stored in the /etc/yum.repos.d, and the repository files have a .repo extension. 
* YUM acts as a high-level package manager, but under the hood, it still depends on RPM to manage packages on the Linux system. 
* Unlike RPM, YUM handles package dependencies very well, it's able to install any dependent packages to get the base package installed on the Linux system. 

















