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



## Modules ##
* Ansible works with modules. Modules are small programs that do the actual work.
* Modules get pushed to the target server by control machine.
* They do their job on the target server like install an application, stop a process, apply firewall rules, etc., and when they are done they get removed.
* Modules are very granular. One module does one small specific task.
