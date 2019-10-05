Make MySql installation secure
==============================

In the commandline enter # mysql_secure_installation and press enter
If you have just installed MySql and haven’t set a password the password will be blank so just press enter at the next step
Select Y to set root password for the new database
Enter a root password
Enter Y to remove anonymous users
Enter Y to Disallow root log in remotely
Enter Y to Remove test database and access to it
Enter Y to Reload privilidge tables
Restart the server to ensure changes are applied by entering the following in the commandline
# service mysqld restart
You will receive a message restarting mysqld (via system ctl)
