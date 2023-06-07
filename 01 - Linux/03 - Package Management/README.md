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



## DPKG ##

* dpkg stands for the Debian package manager and similar to rpm, it is a low-level package manager. Similar to rpm, dpkg can be used to install, remove, upgrade, list, and verify a package. The package extension is .deb. 

* To install or update an existing package, use the dpkg-i <package_name>. 

* To uninstall, use the -r flag. 

* To list packages installed in the system along with the version number in a short description, use the -l flag. 

* Use the -s option to check the status of the package if it is installed in the system. 

* Finally, use the -p flag to display details about packages such as version number, maintainer, et cetera. 

* Similar to rpm, dpkg does not honor the dependencies when it comes to package management. An install may fail due to dependencies issues. This is the reason why we use higher-level Debian package managers such as apt and apt-get. Instead of of relying on dpkg, you can install software along with its dependencies using apt or apt-get. Although it sounds similar, apt and apt-get do not depend on each other. apt stands for advanced package managers is more user friendly and overall a better tool compared to apt-get. 



## APT ##

* apt acts as a front end package manager that relies on the dpkg utility, quite similar to the relation between yum and rpm that we saw earlier. 

* Similar to yum, apt relies on a software repository that contains packages that would eventually be installed on the system. The software repository for apt is defined in the /etc/apt/sources.list file. The source can be a local one such as a directory on the file system or a CD-ROM, or it can be at a remote location that is accessed via HTTP, HTTPS, or FTP transfer protocols. 

* Let us now see some of the common apt commands. 

   1. Run the apt update command to refresh the repository. This command is used to download package information from all available sources. A good time to run this would be immediately after installing the OS or after adding new sources. 
   2. The apt upgrade command can be used to install available upgrades of all packages currently installed on the system from the sources configured. 
   3. You can also update the repositories using the apt edit sources command. This opens up the /etc/apt/sources.list file in the text editor of your choice such as vim or nano. Another way to add more repositories, update the sources.list file directly using a text editor such as the VI-editor. Once the repositories have been set up, you can make use of it to run apt commands. 
   4. To install a package, run the apt install command. 
   5. Run the apt remove command to remove the package. 
   6. The apt search command can be used to look for a package in the repository. 
   7. You can also list all the available packages using the apt list command. 



## APT vs APT-GET ##

* APT is a more user friendly tool compared to APT-GET. In all the latest Debian-based distros, APT is already installed by default.
