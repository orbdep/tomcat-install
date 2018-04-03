## Standalone Tomcat Server

- Requires Ansible 1.2 or newer
- Expects RHEL 6.x/7x hosts

This is a modification to deploy a basic Tomcat server, with very 
basic configuration.  You need ansible installed, and access to the 
hosts via root.  edit the hosts file to point to the servers that you 
want to install a tomcat user on, and this will download the 
dependencies and start a tomcat7 server on that host.  You can change
the ports that will be used in the group_vars/tomcat-servers file 
You will also need to change the username and password in the hosts
file.  You can comment these out if you have SSH keys installed on the
system you're trying to access.

Then run the playbook, like this:

	ansible-playbook -i hosts site.yml -v

When the playbook run completes, you should be able to see the Tomcat
Application Server running on the ports you chose, on the target machines.

This is a very simple playbook and could be the starting point for additional 
tomcat installation playbooks. 

