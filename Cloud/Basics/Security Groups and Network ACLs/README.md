* Security Groups and Network Access Control Lists (NACLs) are types of firewalls that you can use to protect your resources on AWS.

* A Security Group is applied at the instance level. We can apply a Security Group to an instance or multiple instances to control the traffic that we allow to reach or to leave from that EC2 instance.

* NACLs applies at the subnet level. It only restricts traffic whenever it's coming in or out from the subnet. 

* For example, when you send traffic from one instance to another instance within the same subnet, the NACL won't see the traffic but the Security Group will.


