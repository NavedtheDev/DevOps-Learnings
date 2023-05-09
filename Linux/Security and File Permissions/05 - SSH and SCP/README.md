# SSH #

* SSH is used for logging into and executing commands on a remote computer. Syntax.

```
ssh <hostname 0R IP_Address>
```

* Also, you can pass in the user you want to connect to by,

```
ssh <user>@<hostname OR IP_Address>

            OR

ssh -l <user> <hostname OR IP_Address>
```

<b>NOTE:</b> The remote server should have an SSH service running in port 22 accessible from the client for the connection to work. Another requirement is a valid username and password created on the remote system that you can use or something known as an SSH key that we can use to login to the remote machine without a password. 

* These ways discussed above ask for password every time. But, if you do not want to pass in a username and password everytime, you can implement the password-less authentication. 

## Password-less Authentication ##

* To do this, we need to first generate a key pair on the client. A key pair, consists of two pairs of keys, a private key and a public key. 

   1. <b>Private Key:</b> This is the key only you as the client will have and is not shared with anyone else. 
   2. <b>Public Key:</b> It can be shared with others, including our remote server. When it is installed on the remote server, you can unlock it by connection to it with a client that already has the private key. 


* To setup a password-less authentication, 

   1. Create the key pair on the client, which is your laptop using this command,
   ```
   ssh-keygen -t rsa
   ```
   When you run this command, it will ask you to enter a passphrase. It is optional, but improves the security of the key. Only downside of having a passphrase is then having to type it in each time you use the key pair. 
   2. Next step is to copy the public key o the remote server. You have to go through password-based authentication atleast once. Use this command syntax,
   ```
   ssh-copy-id <user>@<hostname OR IP_Address>
   ```
   Once you enter this command, you will be asked to enter the password for your user on the remote server. After this, you will be able to access the remote server without entering a password. 



# SCP #

* SCP allows us to copy data over SSH. This means that you can copy files and directories between your laptop and any other server to which you have SSH access. Example,

```
scp /home/naved/example.txt prodapp01:/home/naved
```
<b>NOTE:</b> You should have permission to write to the directory in the destination, else you will get a permission denied error. 

* If you want to copy directories instead of files, use -r option. 

* To preserve the ownership and permission of the source file, use -p flag. 
