Installing Wordpress in Centos
------------------------------

Install dependencies
======================

Start the terminal and login as root user
Install php dependencies that will allow WordPress to work
# yum -y install php -gd (in order to work with images, install plugins etc…
)
# yum -y install php -xml
# yum -y install wget

Install WordPress
======================
In the commandline enter #pwd to show the directory you are currently in
In the commandline change director cd var/www/html
Download WordPress using the wget command:
# wget http://wordpress.org/latest.zip
Make a Wordpress upload directory
# mkdir -p var/www/html/wordpress/wp-content/uploads

Create MySql database for WordPress
======================

Login to mysql

# mysql -u root -p

Enter the password

N.b. to view databases enter show databases; in the commandline

Create the database by entering the following commands

mysql> CREATE DATABASE wordpress;
mysql> GRANT ALL PRIVILEGES on wordpress.* to 'wpuser'@'localhost' identified by 'your_password';
mysql> FLUSH PRIVILEGES;
mysql> exit

Restart mysql
# systemctl restart mysqld.service

Configure WordPress
======================

Unzip wordpress

unzip the WordPress zip file in the /var/www/html/ directory.
# unzip -q latest.zip -d /var/www/html/

Set the proper permissions:
# chown -R apache:apache /var/www/html/wordpress
# chmod -R 755 /var/www/html/wordpress

create the upload directory manually:
# mkdir -p /var/www/html/wordpress/wp-content/uploads

Allow the Apache web server to write to the uploads directory. 
Do this by assigning group ownership of this directory to your web server which will allow Apache to create files and directories. Issue the following command:
# chown -R :apache /var/www/html/wordpress/wp-content/uploads

Create wp-config file
Enter the WordPress directory:
# cd /var/www/html/wordpress/

Rename wp-config-sample.php into wp-config.php:
# mv wp-config-sample.php wp-config.php

Open the WordPress configuration file in VI editor and change the database values
# vim wp-config.php
