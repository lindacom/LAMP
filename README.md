# LAMP
Setting up a local Linux LAMP environment

Steps
========

1. Install Centos 7 or Dabian on an Oracle Virtual Box
2. Set up the LAMP environment - Linux, Apache, MySql, PHP using the command line
3. Install Wordpress in the LAMP environment

Installing a virtual box
==========================
•	Go to virtualbox.org
•	Click the download link
•	Click the link to install on Windows
•	Once downloaded download the linux centos IOS file by going to centos.org, download the dvd iso file, select a mirror link from the list to download.
Install a virtual machine in your virtual box
==========================
•	In the oracle virtual box click the new icon on the toolbar to add the operating system. Name – Centos, type – Linux, version – Redhat (64 bit)
•	Configure the memoy size – increase memory size to 2048mb (or other)
•	Click next
•	Create a virtual hard drive – accept the default settings
•	Click the create button
•	Specify a hard drive file type – select VD1 virtual disk image
•	Click next
•	Specify storage on physical drive – choose dynamically allocated
•	Click next
•	Specify file location and size (8mb min for centos, select 20.13gb (or other)
•	Click create
•	Centos virtual machine will now be created in the virtual box
Configure virtual box settings
==========================
•	In the Oracle virtual box click the settings button on the toolbar
•	In the general screen click the advanced tab
•	Set both shared clipboard and drag and drop to directional (so that you can copy from other systems to the virtual box)
•	In the systems screen click the processor tab and change processor setting to use 2CPU
Linking machine to virtual box
==========================
•	In the Oracle virtual box select the machine from the left-hand pane
•	On the storage screen select controller – IDF > empty
•	In the attributes > optical drive field click the disc icon and select ‘choose a virtual CD DVD disk drive’
•	Copy the path where centos IOS is located on your computer and click open 
•	Click ok
Running the virtual machine
==========================
•	In the virtual box select Centos machine from the left hand pane
•	Click the start button in the toolbar
•	Click install Centos link (or let it automatically reboot)
•	In the welcome screen select the language
•	Click the next button
Configuring machine settings
==========================
•	Date and time – click on map to select location and click done
•	Keyboard – English and click done
•	Language support – English
•	Security > policy – Use default settings
•	Installation service – Use existing Centos settings
•	Software selection – in basic environment select server with GUI and click done
•	Installation destination – ensure automatically configure partitioning is selected and click done
•	Click the begin installation button
N.b. while the installation is running you can create user and password
Setting up user and password
==========================
•	Click the root password icon
•	Enter a password for a root user
•	Click the done button
•	Click the user creation icon
•	Enter a fullname and username
•	Enter a password
•	Check the make user an administrator box
•	Click done
Reboot the machine
==========================
When the installation is complete and before rebooting you need to unmount centos. To do this 
•	On the virtual box select devices > cd dvd devices and uncheck centos. 
•	Click force unmount button. 
•	Click reboot button
•	On the virtual box select machine > reset and click the restart button
•	Select the first Centos Linux option and the machine will restart
•	Enter 1 and then enter 2 to accept the licence agreement
•	Press Q to quit
•	Press enter
•	Press yes to reboot

