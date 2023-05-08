* Most of the access control files in linux are stored under the /etc directory. This directory can be read by any user by default, but only the root user has access to write to it. 

* They are also designed in a way that they should never be modified using a text editor. Instead, use the built-in commands to add or modify access as needed. We will learn how to do that later.

* Let us look at the basic access control files in linux. 

   1. /etc/passwd -> commonly known as the password file. It contains basic information about the users in the system. Note that this file does not store any passwords. File structure is like,
   ```
   USERNAME:PASSWORD:UID:GID:GECOS:HOMEDIR:SHELL
   ```
   2. /etc/shadow -> password are stored here. Contents of this file are hashed. File structure is like,
   ```
   USERNAME:PASSWORD:LASTCHANGE:MINAGE:MAXAGE:WARN:INACTIVE:EXPDATE
   ```
   3. /etc/group -> stores information about all user groups on the system such as group name, gid and members. File structure is like,
   ```
   NAME:PASSWORD:GID:MEMBERS
   ```
