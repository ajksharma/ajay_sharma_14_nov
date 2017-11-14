# ajay_sharma_14_nov
  

# Problems

### Assignment 1 :

Write a Dockerfile (CentOS 6) to install the following in a Docker continer:

Python 2.7

MongoDB - any version

Apache tomcat 7 - running on port 8080

Please include comments at every command explaining what it does.

Write the command to run the Dockerfile such that once the container boots, apache tomcat's home page is accessible from the host on port 7080.
### Answer :Dockerfile -> https://gist.github.com/ajksharma/7a66e8fcdc9b780c13e76b96bca1e528#file-dockerfile
### Run it as -> docker run -it -p 7080:8080 centos6/tomcat7

### Assignment 2 :

Write a bash/python script that takes list of hostnames (comma separated) as an argument.

This script, when executed, should connect to all the servers via. SSH (standard port) (assume password-less connectivity) and give a single prompt to the user.

When the user executes a command on this prompt, the script should run the command on all connected servers and display the output.

Make this as efficient as possible, code comments appreciated.

### Answer : I have written an ansible script instead. Hope that doesn't matter. Though I know python & bash too, ansible for now seems the right tool for this task.
### Host file : https://gist.github.com/ajksharma/fab151c7c561d87ddf4faa11052f34c5#file-hosts
### Ansible command : $ ansible all -a "/sbin/reboot" -f 10     (this rusn the command on all servers in a group, in this case, "all" from the hosts file parallely in 10 forks)


### Assignment 3 :

Consider a monolithic java application stack.

Apache Web Server, Apache Tomcat application server with Active MQ and Oracle and MongoDB backend.

Propose a solution to migrate this application stack to cloud of your choice (AWS/OpenStack/Azure).

Mention all the provider services you would use and how you would maintain HA and Load Balancing (consider app to be stateless). Mention rationale for each decision.
