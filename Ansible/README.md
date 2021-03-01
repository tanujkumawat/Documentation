# Install Ansible

## 1. Update the system packages to the latest versions:

	$ sudo apt update 
	$ sudo apt upgrade
  
## 2. Now we will install the Ansible PPA repository on the system using below command:
  
  $ sudo apt install software-properties-common
  $ sudo apt-add-repository --yes --update ppa:ansible/ansible
  
## 3. Install Ansible:
  
  $ sudo apt install ansible -y

check version:

  $ ansible --version
  
# Setup Ansible host file

  $ sudo vim /etc/ansible/hosts
  
          /etc/ansible/hosts
  
  [nodes]
  "node_ip" ansible_user="user" ansible_password="password" 
  
  Example: 
  
  [node]
  172.17.0.2 ansible_user=root ansible_password=root
