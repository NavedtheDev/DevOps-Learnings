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
