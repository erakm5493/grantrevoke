# grantrevoke
Automate the process of granting / revoking SSH access to a group of servers instances to a new developer

ssh-access

1.Command to add new user and grant SSH access

ansible-playbook -i inventory/ -e "action=grant" playbook/grantrevoke.yml


Command to revoke SSH access from a user

ansible-playbook -i inventory/ -e "action=revoke" playbook/grantrevoke.yml --skip-tags=remove

********************************************************************************
** Server instance can be changed under 

inventory/hosts  

[server]

your desired instance1
your desired instance2

********************************************************************************** "user_name" and "user_des" can be changed as per requirment

********************************************************************************user name of instance can be changed in grantrevoke.yml .Default here is used as ubuntu.
*******************************************************************************
