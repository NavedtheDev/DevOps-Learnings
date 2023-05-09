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
