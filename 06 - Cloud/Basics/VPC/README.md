* The Amazon Virtual Private Cloud is a virtual space into which you can launch your resources.
* So you will be creating your own VPCs within AWS. There is also a default VPC created for you.



## What a VPC actually is ? ##

-> A VPC is a logically isolated portion of the cloud within a region. You can have multiple VPCs in a region. <br>

-> You can then create subnets within your VPC and they are actually assigned to an availability zone. So you can create subnets that are sitting in different data centres and deploy your resources there. One subnet is created per availability zone. So you will have the number of subnets same as the number of availability zones. <br>

-> We use a VPC Router to actually send information between our resources in different subnets within our VPC. And the way that we can manipulate the router and configure it so that it sends data to the correct locations is by using <b>Route Table</b>. <br>

-> So we create route tables and assign them to our subnets. <br>

-> An Internet Gateway is used to connect to the internet. <br>

-> Here we need to understand the Public subnets and the Private subnets. <br>

<b>Public Subnet:</b> The instances here will get a public IP address and can use the Internet Gateway directly to access the internet. <br>
<b>Private Subnet:</b> The instances here can't access the Internet Gateway directly.
