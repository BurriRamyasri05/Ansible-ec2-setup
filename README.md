# Ansible-ec2-setup
Configured Ansible control node on EC2 and established connection to target server
Overview:
This project explains how i configured Ansible on an Ubuntu Ec2 instance and established a connection to the target server without using password.

Architecture:
Control node: Ubuntu EC2(Ansible installed)
Target Node: Ubuntu Ec2

Steps performed:
Connect to the ansible server via ssh -i keyfile servername@publicip
generate the keys using the ssh-keygen 
now copy the public key of the ansible server 
Connect to the target server in a duplicate cmd 
follow the same steps to generate the keys 
now update the autorised keys of the target server with the public key of the ansible server
once done ssh into the target ip address from the ansible server 
and now to install nginx into the target server
create an inventory file and the playbook file on the ansible server and  run the ansible-playbook -i inventory playbook.yaml
this commmand will reflect the actions which are mentioned as part of the playbook to teh target server
so on target server this can be verified by doing systemctl status nginx


Output

Successfully established connection between Ansible control node and target server.
