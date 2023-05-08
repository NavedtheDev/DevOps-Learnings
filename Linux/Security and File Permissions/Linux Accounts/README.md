## User Account ## 

* A user account refers to individual people who need access to the linux system. 

## Superuser Account ##

* A super user account is the root which has the UID 0. The superuser has unrestricted access and control over the system, including other users. 

## System Accounts ##

* They are usually created during the OS installation. These are for use by software and services that will not run as the super user. SSHD and the mail user are examples. 

## Service Accounts ##

* They are similar to system accounts and are created when services are installed on linux. Example, an nginx server makes use of a service account called nginx. 



* To see details about users in the linux system, we use some basic commands.

   1. id -> gives information about the user specifically the uid, gid, and groups a user is part of. 
   2. who -> to see the list of users currently logged into the system.
   3. last -> displays the record of all logged-in users. It also shows the date and time when the system was rebooted.
   
   

## Switching Users ##

* su -> with this command. you can switch to any other user in the system, including root. 
