* To run a command( application or a script ) in the background, we have to define it as a service. For this we create a service unit file. 

* This unit file needs to be created under /etc/systemd/system directory.

* Example,

![Screenshot (154)](https://github.com/NavedtheDev/DevOps-Learnings/assets/98219227/80fb692f-28e4-40c0-bfd7-50471be5c03a)


* To run this service in the background, use, 

```
sudo systemctl start project-mercury.service
```

* To check it's status,

```
sudo systemctl status project-mercury.service
```

* To stop the service,

```
sudo systemctl status project-mercury.service
```

* To allow the above service to be enabled during boot, add another section called install. 

* Here is a complete example,

![Screenshot (156)](https://github.com/NavedtheDev/DevOps-Learnings/assets/98219227/4971eabe-f4b0-462c-ba06-39d56c936a3d)

* For the system to detect the changes, use the command,

```
sudo systemctl deamon-reload 
```

then,

```
sudo systemctl start project-mercury.service
```
