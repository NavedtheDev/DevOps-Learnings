* iptables is a command-line utility for configuring the firewall in Linux-based operating systems.

* It provides a powerful and flexible framework for managing network traffic by defining rules and policies.

* iptables allows you to set up rules to filter, modify, and route network packets, giving you control over incoming and outgoing traffic on your system. 

* To install iptables on Ubuntu, use the command,

```
sudo apt install iptables
```

* To list the default rules,

```
sudo iptables -L
```

* We will see three types of rules or chains configured by default after running above command, input, forward and output. 

   1. The input chain is applicable to network traffic coming into the system. 
   2. The output chain is responsible for connections initiated he system to other systems. 
   3. Forward chain is used in network routers where the data is forwarded to other devices in the network. It is not commonly used in a linux server. 

* They are called chains because each chain can have multiple rules within it. Each rule performs a check and accepts or drops the packet based on the condition.



![Screenshot (148)](https://github.com/NavedtheDev/DevOps-Learnings/assets/98219227/39865ed9-ba8c-43fc-b84d-26657f949b43)



* Example of creating an input rule on a dev server,

```
sudo iptables -A INPUT -p tcp -s 172.18.216.10 --dport 22 -j ACCEPT
```

* If we use -I option instead of -A, it will insert the rule to the top of the chain instead of the bottom. 


![Screenshot (159)](https://github.com/NavedtheDev/DevOps-Learnings/assets/98219227/c8e88fea-2dfc-4442-ace3-878a7668d99c)


<b>NOTE:</b> Sequence in which we add rules is very important. They are implemented from top to bottom. 



* To delete a rule, use -D option. For example, to delete a rule at posiion 3, 

```
iptables -D OUTPUT 3 
```
