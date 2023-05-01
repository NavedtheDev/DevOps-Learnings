* The Linux shell is a program that allows text-based interaction between the user and the operating system. This interaction is carried out by typing commands into the interface and receiving the response in the same way. 
* The Linux shell is a powerful tool with which you can navigate between different locations within the system. When you log into the shell, the very first directory you are taken to is your home directory. 
* /home is a system created directory that contains the home directories for almost all users in the Linux system. 
* Why do we need a home directory? The home directory allows users to store their personal data in the form of files and directories. Each user in the system gets their own unique home directory with complete access to it, to be able to save, retrieve, or delete data. 
* Another thing to note is the representation of the home directory. It is represented by the tilde symbol ( ~ ) in the command line. 
* To interact with the Linux system using the shell, a user has to type in commands. When a command is run, it executes a program to achieve a specific task. 
* An arguement acts as an input to a command. 
* A command can also have options that modify its behavior in some predetermined way. This option, also sometimes referred to as a switch or a flag, is usually a single letter preceded by a single hyphen.
* Commands in Linux can be generally categorized into two types, internal, or built-in, commands and external commands. 
* Internal commands are part of the shell itself and come bundled with it. 
* External commands, on the other hand, are binary programs or scripts which are usually located in distinct files in the system. They either come pre-installed with the distribution's package manager or can be created or installed by the user. 
* To determine if a command is internal or external, use the "type" command. For example,

```
type cd
```

* Output will be, 

```
echo is a shell builtin
```

* NOTE: There are three parts in a Linux sentence

```
<command> <arguement> <option>
```
