# What is Ansible? #
* Ansible is simple open source IT engine which automates applicatiopn deployment, intra service orchestration, cloud provisioning and many other IT tools.
* Suppose an organization has 100's of systems, and given one or even a small team of people the responsibility to configure all the systems makes their work really tough and repetitive. ALso, manual work is prone to errors. Comes into picture Ansible, which can automate the configuration of all the systems.
* Ansible do so by 4 different ways:

       1. Execute taks from your own machine instead of SSH into all remote servers.
       2.  Configuration/Installation/Deployment steps in a single YAML file instead of manual and shell scripts.
       3.  Re-use same file multiple times anf dor different environments.
       4.  More reilable and less likely for errors.



## Ansible is agentless ##
* Normally when you want to use some tool on a machine you need to go to that machine and install an agent for that tool. However, to use Ansible you don't have to install anything on the target servers, you just install it on your control machine which could be even your laptop. And that machine can now manage all target machines remotely.
* Agentless means that you don't need to install any additional software on the target machines to be able to work with Ansible.
* One of the major disadvantages of most other orchestration tools is that you are required to configure an agent on the target systems before you can invoke any kind of automation.


## Modules ##
* Ansible works with modules. Modules are small programs that do the actual work.
* Modules get pushed to the target server by control machine.
* They do their job on the target server like install an application, stop a process, apply firewall rules, etc., and when they are done they get removed.
* Modules are very granular. One module does one small specific task.
* Ansible has 100's of modules that each execute a specific task. You can see the whole list of Ansible modules in the official documentation.



## Ansible uses YAML ##
* Ansible uses YAML, that is also the reason why it became so popular.
* So it doesn't require learning any special language.



## Ansible Playbooks ##
* To handle a complex application weneed multiple modules in a certain sequence groupef together to represent that one whole configuration, that's where Ansible Playbooks come in.
* So first of all, the sequential modules are grouped in tasks where each task make sure the module get executed with certain arguements.
* Now we have to define where or on which target machine this task should be executed and we do that using the HOSTS attribute. 
* Also, we need to define with which user should the tasks execute.

![Playbook](https://user-images.githubusercontent.com/98219227/209770741-f33f19dd-f9b7-4c52-8b1c-078dd17e6e8a.png)



# Ansible Inventory #
* Ansible can work with one or multiple systems in your infrastructure at the same time. In order to work with multiple servers, Ansible needs to establish connectivity to those servers. This is done using SSH for Linux and PowerShell remoting for windows. That's what makes Ansible agentless. 
* A simple SSH connectivity would suffice Ansible's needs.
* Now, information about the target systems is stored in an inventory file. If you don’t create a new inventory file, Ansible uses the default inventory file located
at /etc/ansible/host location. 
