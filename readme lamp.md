Setting up the LAMP stack
------------------------------

To install, first you must add the Webtatic EL yum repository information corresponding to your CentOS/RHEL version to yum
1.	Install webtatic repo
=========================

•	Go to https://webtatic.com/projects/yum-repository/ 
•	install the webtatic-release RPM: In the commandline enter https://mirror.webtatic.com/yum/el6/latest.rpm

2. Install webtatic LAMP stack
=========================
You can install the LAMP stack all at once or individually.

To install packages individually

A. PHP
=========================
Now you can install PHP 7.0’s mod_php SAPI (along with an opcode cache)

Php – at the commandline enter yum install php70w php70w-opcache


To check what version of php has been installed enter #php –version at the commandline
Upgrading PHP
Unless you know what you are doing, it is risky upgrading an existing system. It’s much safer to do this by provisioning a separate server to perform the upgrade as a fresh install instead.
In the commandline enter yum install yum-plugin-replace
yum replace php-common --replace-with=php70w-common

B. MySql
=========================
To install MySql client and server

My sql and server – at the commandline enter yum install mysql55w mysql55w-server

To check whether MySql and MySql server are installed enter rpm -q mysql mysql-server in the commandline

Upgrading MySql

If you already have MySql client or server installed (to check enter rpm -q mysql mysql-server in the commandline), then you can upgrade using the following method:
yum install mysql.`uname -i` yum-plugin-replace
yum replace mysql --replace-with mysql55w

Removing Maria DB in order to install mysql instead

If you had mariadb installed and you want to remove it then enter
Yum remove mariadb mariadb-server
Yum shell
> Remove mariadb-ls
> Run
> exit


To install the LAMP stack all at once

At the commandline enter # yum -y install –enable repo = webtatic httpd mysql -server mysql php55w php 55w -mysql 
N.b. see the webtatic website for the most up to date command
