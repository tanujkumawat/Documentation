## 1. Update the system packages to the latest versions:

	$ sudo apt update 
	$ sudo apt upgrade

## 2. Install Nginx Package:

	$ sudo apt install nginx

####    Note: For specific version
	
	$ sudo apt install nginx=version

## 3. Start and Enable Nginx service:

	$ sudo systemctl start nginx
	$ sudo systemctl start nginx

## 4. Install PHP & PHP_FPM:

	$ sudo apt install php
	$ sudo apt install php-fpm

####    Note: For specific version

	$ sudo apt install php7.2
	$ sudo apt install php7.2-fpm
	
## 5. Start & Enable php-fpm:
	
	$ sudo systemctl start php-fpm
	$ sudo systemctl enable php-fpm

## 6. Install PHP modules:

	$ sudo apt install libapache2-mod-php php-mbstring php-xmlrpc php-soap php-gd php-xml php-cli php-zip php-bcmath php-tokenizer php-json php-pear

## 7. Install MySQL Database:

	$ sudo apt install mysql-server
	
After that, you can set a password for the root. To do this, you need to use the mysql_secure_installation script. Keep in mind that this step is optional, but recomended for security reasons.

	$ sudo mysql_secure_installation

## 8. Install Composer:

	$ sudo apt install curl 
	$ curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
	
Check composer installed or not

	$ composer
 
