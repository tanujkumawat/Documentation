# Install Ansible

### 1. Update the system packages to the latest versions:
	$ sudo apt update 
	$ sudo apt upgrade
  
### 2. Now we will install the Ansible PPA repository on the system using below command:
  	$ sudo apt install software-properties-common
  	$ sudo apt-add-repository --yes --update ppa:ansible/ansible
  
### 3. Install Ansible:
  	$ sudo apt install ansible -y

check version:
  	$ ansible --version
  
# Setup Ansible host file
  	$ sudo vim /etc/ansible/hosts
	
Add the line at the start of the file enter the IP of the node and user, password.

	  [nodes]
	  "node_ip" ansible_user="user" ansible_password="password" 

	Example: 

	  [node]
	  172.17.0.2 ansible_user=root ansible_password=root

# Configure Ansible configuration file "ansible.cfg"
	$ sudo vim /etc/ansible/ansible.cfg
	
Go to line 70 and uncomment this line:

	host_key_checking = False
	
# Setup ssh connection between Master and Slave node:
Run this command on Master node

##### Generate ssh key:
	$ ssh-keygen
	
##### Copy ssh key to host node:
	$ ssh-copy-id User_name@Host_IP


# Now try to ping the host node using ansible:
	$ ansible all -m ping
