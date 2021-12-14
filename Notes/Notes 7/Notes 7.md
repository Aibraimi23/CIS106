# Managing Users and groups
## Managing User Accounts
* Managing user accounts involves adding, modifying and deleting user accounts and account's information
* Add user accounts use useradd or adduser
* modify use usermod
* delete use userdel
* make sure to use sudo
* The /etc/login.defs file contains directives for use in various shadow password suite commands
* The /etc/default/useradd file stores the system default configuration for creating new users with the useradd utility
* to view the default parameters use either
  * useradd -D
  * cat /etc/default/useradd
* The /etc/passwd file stores information about every user account in a Linux system
* The /etc/shadow file contains information about the users' passwords
### Creating a user with useradd
* The useradd utility, in Ubuntu, is considered a low-level utility and should not be used. This utility is the standard in most linux distros. The adduser utility uses the useradd utility in the "backend".
* -md options needed for adding a home directory to a user
* /home/student is the new users home directory
* -s used for specifying the users login shell
* /bin/bash is the new users login shell
* students is the users username
### Viewing a user's account info
* The grep command is used to see the students user information - grep student /etc/passwd/
* The second one is used to see password information about the new user. ! means there is no password set - sudo grep student etc/shadow/
* The third shows the content of the students user home directory - ls -A /home/student/
* the fourth shows the content of the skel directory which must be the same as the new user's home directory - sudo ls -A /etc/skel/
* The getent utility can be used to view information about a user's account and password - getent passwd student - sudo getent shadow student
### Maintaining Passwords
* The useradd does not create a password for the users, the passwd utility does
* To change password of another user - passwd + username
* to change password of the current user - passwd with no argument 
* The passwd utility can also lock and unlock account with the -l and -u options
* -d delete
* -e expire
* -i inactive
* -l lock
* -n minimum 
* -s status
* -u unlock
* -w warning or warndays
* -x maximum or maxdays
* Chage is also another utility to work with passwords
  * It can modify and display user information
### Deleting User Accounts
* userdel utility and the most common option to use is -r 
* This option will delete the accounts home directory tree and any files within it
* Delete the sampleuser account sudo userdel -r sampleuser
## Managing Groups
* sudo group user shows the group name that the usr belongs to.
* to create a new group - sudo groupadd groupname
* To add a user to a new group add, the group must preexist - sudo getent group groupname
* sudo usermod -aG groupname user allows you to add the DAdams account as a member of the project42 group but the -a switch is important because it preserves only previous DAdams account group memberships
### Delete me
* Groups can also have passwords but is not a good idea
* The /etc/shadow/ file is where group passwords are stored
* If you need to modify a group us groupmod - sudo groupmod then whatever variable you need.
## Querying Users
* Whoami displays what user account you are currently using
* Who provides a little more data than whoami utility. You can view information concerning your own account or look at every current user on the system.
* W shows who is logged on and what they are doing
* Id utility allows you to pull out various data concerning the current process. it also displays information for any account whose identification you pass to id as an argument
* Last pulls information from the /var/log/wtmp fie and displays a list of accounts showing the last time they logged in/out the system or if they are still logged on. It also shows when the system reboot occurs and when the wtmp file was started