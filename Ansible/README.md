# What is Ansible? #
* Ansible is simple open source IT engine which automates applicatiopn deployment, intra service orchestration, cloud provisioning and many other IT tools.
* Suppose an organization has 100's of systems, and given one or even a small team of people the responsibility to configure all the systems makes their work really tough and repetitive. Also, manual work is prone to errors. Comes into picture Ansible, which can automate the configuration of all the systems.
* Ansible do so by 4 different ways:

       1.  Execute tasks from your own machine instead of SSH into all remote servers.
       2.  Configuration/Installation/Deployment steps in a single YAML file instead of manual and shell scripts.
       3.  Re-use same file multiple times for different environments.
       4.  More reilable and less likely for errors.



# Ansible is agentless #
* Normally when you want to use some tool on a machine you need to go to that machine and install an agent for that tool. However, to use Ansible you don't have to install anything on the target servers, you just install it on your control machine which could be even your laptop. And that machine can now manage all target machines remotely.
* Agentless means that you don't need to install any additional software on the target machines to be able to work with Ansible.
* One of the major disadvantages of most other orchestration tools is that you are required to configure an agent on the target systems before you can invoke any kind of automation.


# Modules #
* Ansible works with modules. Modules are small programs that do the actual work.
* Modules get pushed to the target server by control machine.
* They do their job on the target server like install an application, stop a process, apply firewall rules, etc., and when they are done they get removed.
* Modules are very granular. One module does one small specific task.
* Ansible has 100's of modules that each execute a specific task. You can see the whole list of Ansible modules in the official documentation.



# Ansible uses YAML #
* Ansible uses YAML, that is also the reason why it became so popular.
* So it doesn't require learning any special language.



# Ansible Playbooks #
* Ansible playbooks are Ansible's orchestration language. It is in playbooks where we define what we want Ansible to do. It is a set of instructions you provide Ansible.
* For example, it can be as simple as running a series of commands on different servers in a sequence restarting those servers in a particular order or it could be as complex as deploying hundreds of VMs in a public and private cloud infrastructure.
* A playbook is a single YAML file containing a set of plays. A play defines a set of activities to be run on a single or a group of hosts.
* A task is a single action to be performed on a host. The different actions run by tasks are called modules.
* The playbook is a list of dictionaries in YAML terms. Each play is a dictionary and has a set of properties called name, hosts, and tasks. The host parameter indicates which hosts you want these operations to run on.



# Ansible Inventory #
* Ansible can work with one or multiple systems in your infrastructure at the same time. In order to work with multiple servers, Ansible needs to establish connectivity to those servers. This is done using SSH for Linux and PowerShell remoting for windows. That's what makes Ansible agentless. 
* A simple SSH connectivity would suffice Ansible's needs.
* Now, information about the target systems is stored in an inventory file. If you don’t create a new inventory file, Ansible uses the default inventory file located
at /etc/ansible/host location. 
* The inventory file is in an INI-like format. It's simply a number of servers listed one after the other. You can also group different servers together.
* In inventory files we have different parameters. 

                1. Ansible_host is an inventory parameter used to specify the FQDN or IP Address of a server.
                2. Ansible_connection is what defines how Ansible connects to the target server.
                3. Ansible_port defines which port to connect to. By default, it is set to port 22 for SSH, but if you need to change you can set it differently.
                4. Ansible_user defines the user used to make remote connections. By default, this is set to root for Linux machines.
                5. Ansible_ssh_pass defines the SSH password for Linux.



# Ansible Variables #
* Variables in Ansible store information that varies with each host. 
* To add a variable we could simply add a vars directive followed by variables in a key-value pair format.
```
vars:
   dns_server: 10.1.250.10
```
* We can also have variables defined in a separate file dedicated for variables. 
* So how do we use variables ? Here is an example.
```
-
   name: Add DNS server to resolv.conf
   hosts: localhost
   vars:
       dns_server: 10.1.250.10
   tasks: 
       - lineinfile:
             path: /etc/resolv.conf
             line: 'nameserver {{ dns_server }}'
```
* Remember that this format we are using to use variables in playbooks is called Jinja2 Templating.
* While using variables with Jinja2 Templating, remember to enclose it within quotes. However, if the variable is in between sentences then that is not required.



# Ansible Conditionals #
* We could use the when conditional statement to specify a condition for each task. Only if the condition is true, that task will run. 
* Here is an example.
```
- name: Install NGINX
  hosts: all
  tasks:
   - name: Install NGINX on Debian
    apt:
      name: nginx
       state: present
    when:
           ansible_os_family == "Debian"
  - name: Install NGINX on Redhat
    yum:
      name: nginx
       state: present
    when:
           ansible_os_family == "RedHat"
```

* Make sure to use == sign when checking equality in conditional statement. 
* You may use an OR operator to specify either of two conditions. 
* AND operator must satisfy both conditions. 
* You may use conditionals in a loop as well. Here is an example
```
- name: Install Softwares
  hosts: all
  vars:
     packages:
         - name: nginx
          required: True
         - name: mysql
          required : True
         - name: apache
          required : False
  tasks:
   - name: Install "{{ item.name }}" on Debian
     apt:
       name: "{{ item.name }}"
       state: present
     when: item. required == True
     loop: "{{ packages }}"
     
```



# Ansible Loops #
* Look at this example where we are creating an Ansible Playbook to create users in a system using the user module. The user module helps you create users on the target systems. 
```
-
   name: Create users
   hosts: localhost
   tasks:
     - user: name=Virat   state=present
```
* Here we have created just one user. What if we want to create multiple users?
* One way to do this would be to duplicate the lines as many times as required. 
```
-
   name: Create users
   hosts: localhost
   tasks:
     - user: name=Virat  state=present
     - user: Virat       state=present
     - user: Sachin      state=present
     - user: Rohit       state=present
     - user: Hardik      state=present
     - user: Rishabh     state=present
     - user: Rahul       state=present
```
* But this is not an efficient way. A better way to do this would be to have a single task loop over all the users. Here comes into picture Loops.
* Loop is a looping directive that executes the same task multiple number of times. Each time it runs, it stores the value of each item in the loop in a variable. Consider this example.
```
-
   name: Create users
   hosts: localhost
   tasks:
     - user: name='{{ item }}'  state=present
       loop:
         - Virat 
         - Sachin
         - Rohit
         - Hardik
         - Rishabh
         - Rahul
```
* You can simply replace the username, in this case Virat, with the item variable inside double braces. 
* The loop directive we just saw are used to create simple loops that iterate over a lot of items. There's another way to create loops in playbooks, that is using the with_ directives.
* The playbook that we developed can also be written using the with_items directive.
```
-
   name: Create users
   hosts: localhost
   tasks:
     - user: name='{{ item }}'  state=present
       with_items:
         - Virat 
         - Sachin
         - Rohit
         - Hardik
         - Rishabh
         - Rahul
```
* Both the playbooks give the same results.
