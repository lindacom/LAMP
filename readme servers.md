Running the servers
----------------------
Check that servers are ready
==============================
To check that the servers are ready enter the following at the commanline
# chkconfig httpd on (press enter). You will receive a message – note forwarding request to ‘systm ctl enable http service’
Then enter
# chkconfig mysqld on (press enter)

Open a browser session
=========================
•	In the machine open another screen and select applications > firefox to open a browser session
•	In the browser address bar enter localhost
Turn on the web server and database server
In the command line start the servers by entering the following
# service httpd start – you will receive a message redirecting to /bin /system ctl start httpd service then enter
# service mysqld start – you will receive a message starting mysqld (via system ctl)
Nb. If maria db is installed enter mariadb instead of mysqld

Create a php file to test the server
====================================

In the command line enter 
# vi /var /www /html /index.php to use the vim editor to create an index file
In the file press I to enter insert mode
Enter the following code in this new file
<?php
phpinfo();
?>
Press the esc key to exit insert mode
Type :wq and press enter to save the file or press shift +zz to save and exit
In the second window refresh the browser to see a php info page now displayed. This sows that the servicer is now displaying the index file.

