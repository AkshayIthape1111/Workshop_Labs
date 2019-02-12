# Managing local linux users and groups 
Linux is a multi-user operating system, which means that more than one user can use Linux at the same time. Linux provides a beautiful mechanism to manage users in a system. One of the most important roles of a system administrator is to manage the users and groups in a system.
## What Is User
Every process on the system runs as a particular user and every file is owned by a particular user. A user or account of a system is uniquely identified by a numerical number called the UID (unique identification number). There are three types of users 
1. The root or super user 
This is also called superuser and would have complete and unfettered control of the system. A superuser can run any commands without any restriction. This user should be assumed as a system administrator.
2. System users
System accounts are those needed for the operation of system-specific components for example mail accounts and the sshd accounts. These accounts are usually needed for some specific function on your system, and any modifications to them could adversely affect the system.
3. Normal users
User accounts provide interactive access to the system for users and groups of users. General users are typically assigned to these accounts and usually have limited access to critical system files and directories.

The full account information is stored in the **/etc/passwd** file and a hash password is stored in the file **/etc/shadow**.
## What Is Group
Linux group is a mechanism to organise a collection of users. Like the user ID, each group is also associated with a unique ID called the GID (group ID). There are two types of groups 
1. A primary group
2. A supplementary group

Each user is a member of a primary group and of zero or ‘more than zero’ supplementary groups. <br/>
The group information is stored in **/etc/group** and the respective passwords are stored in the **/etc/gshadow** file.
## id command 
Print user and group information for the specified USERNAME or for the current user.<br/>
On its own the id command prints a lot of information:
* user id
* username
* group id
* group name
* id of other groups
* names of other groups
```
command :- id
output :- uid=1000(akshay-devops) gid=1000(akshay-devops) groups=1000(akshay-devops),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),113(lpadmin),128(sambashare),130(libvirtd),999(docker)
```
## useradd and usermod command 
There are times when a Linux System Administrator asked to create user accounts on Linux  with some specific properties, limitations or comments.<br/>
In Linux, a ‘useradd‘ command is a low-level utility that is used for adding/creating user accounts in Linux and other Unix-like operating systems. The ‘adduser‘ is much similar to useradd command, because it is just a symbolic link to it.<br/>
When we run ‘useradd‘ command in Linux terminal, it performs following major things:
1. It edits following files for the newly created User account .
   * /etc/passwd
   * /etc/shadow
   * /etc/group
   * /etc/gshadow 
2. Create a group with same username or if you specify group and it will add your new user to that particular group .
3. Creates and populate a home directory for the new user.
4. Add all files to home directory which required for your new user login . files like .bashrc, .bash_profile, .history etc .
5. Sets permissions and ownerships to home directory.

Some examples :-
1. **useradd Salu** - It create Salu user in your system .
2. **passwd Salu** - By using passwd command we set the passwd to the new user (Salu) .
3. **useradd -d /home/Redhat/ Salu** - 
   * It create a new user Salu and assign it home directory in /home/Redhat directory with it name .
   * -d option is use to specify the directory and default it create user directory in /home .
4. **useradd -u 999 Salu**
   * It create new user Salu with uid 999 . uid is used by kernel for processing and default uid provide by kernel to user when we created user .
   * -u option is useful when we want assign uid to that user .
5. **useradd -u 1000 -g 500 Salu**
   * It create a new user with uid 1000 and gid 500 . gid is group id .
   * -g option is used to assign gid .
6. **useradd -Gredhat,focus,engg Salu**
   * The ‘-G‘ option is used to add a user to additional groups. Each group name is separated by a comma, with no intervening spaces.
7. **useradd -M Salu**
   * where we don’t want to assign a home directories for a user’s, due to some security reasons. In such situation, when a user logs into a system that has just restarted, its home directory will be root. When such user uses su command, its login directory will be the previous user home directory.
   * To create user’s without their home directories, ‘-M‘ is used.
8. **useradd -e 2014-03-27 Salu**
   * By default, when we add user’s with ‘useradd‘ command user account never get expires i.e their expiry date is set to 0 (means never expired).
   * However, we can set the expiry date using ‘-e‘ option, that sets date in YYYY-MM-DD format. This is helpful for creating temporary accounts for a specific period of time.
9. **useradd -e 2014-04-27 -f 45 Salu**
   * The ‘-f‘ argument is used to define the number of days after a password expires. A value of 0 inactive the user account as soon as the password has expired. By default, the password expiry value set to -1 means never expire.
10. **useradd -c "Hero" Salu**
    * The ‘-c‘ option allows you to add custom comments, such as user’s full name, phone number, etc to /etc/passwd file. The comment can be added as a single line without any spaces.
11. **useradd -s /sbin/nologin Salu**
    * we add users which has nothing to do with login shell or sometimes we require to assign different shells to our users. We can assign different login shells to a each user with ‘-s‘ option.
12. **useradd -u Salu**
    * ‘-U‘ argument create/adds a group with the same name as the user.
13. **useradd -k Salu**
    * we used ‘-k‘ option to set custom skeleton directory i.e. /etc/custom.skell, not the default one /etc/skel.
    * The skeleton directory, which contains files and directories to be copied in the user's home directory, when the home directory is created by useradd.
    * This option is only valid if the -m (or --create-home) option is specified.
14. **useradd -b Salu**
    * The default base directory for the system
    * If this option is not specified, useradd will use the base directory specified by the HOME variable in /etc/default/useradd, or /home by default.
15. **useradd -m Salu**
    * Create the user's home directory if it does not exist. The files and directories contained in the skeleton directory (which can be defined with the -k option) will be copied to the home directory.
    * By default, if this option is not specified and CREATE_HOME is not enabled, no home directories are created.
16. **useradd -ou 1000 Salu**
    * Allow the creation of a user account with a duplicate (non-unique)UID.
    * This option is only valid in combination with the -u option.
17. **useradd -r system**
    * Create a system account.
    * System users will be created with no aging information in /etc/shadow, and their numeric identifiers are chosen in the SYS_UID_MIN-SYS_UID_MAX range, defined in /etc/login.defs, instead of UID_MIN-UID_MAX (and their GID counterparts for the creation of groups).Note that useradd will not create a home directory for such an user, regardless of the default setting in /etc/login.defs(CREATE_HOME). You have to specify the -m options if you want a home directory for a system account to be created.

The system administrator is responsible for placing the default user files in the /etc/skel/ directory (or any other skeleton directory specified in /etc/default/useradd or on the command line).
<br/>
**In usermod command 80% options are same like useradd .**
* -m, --move-home<br/>
Move the content of the user's home directory to the new location.This option is only valid in combination with the -d (or --home)option.usermod will try to adapt the ownership of the files and to copythe modes, ACL and extended attributes, but manual changes might beneeded afterwards.
* -l, --login NEW_LOGIN<br/>
The name of the user will be changed from LOGIN to NEW_LOGIN. Nothing else is changed. In particular, the user's home directory or mail spool should probably be renamed manually to reflect the new login name.
* -a, --append<br/>
Add the user to the supplementary group(s). Use only with the -G option.
## groupadd and groupmod command 
The groupadd command creates a new group account using the values specified on the command line plus the default values from the system. The new group will be entered into the system files as needed.<br/>
When we run ‘groupadd‘ command in Linux terminal, it performs following major things:
1. It edits following files for the newly created User account .
   * /etc/group
   * /etc/gshadow 

Some Examples :-
1. **groupadd Redhat** - It create Redhat group in the system .
2. **groupadd -f javaproject** - if you want to exit the command with success status, when the group exists, use -f or --force option.
3. **groupadd -g 3456 systemd1** - The GID of the added group is decided by the system. But if you want to provide some specific GID, it can be provided with -g or --gid option.
4. **groupadd -r systemd1** - The GIDs allotted to new groups are allocated between GID_MIN and GID_MAX values from login.defs file. Usually, the value of GID_MIN is 500 or 1000 in most systems. The GIDs below GID_MIN are reserved for system groups. If a system group is needed to be created, use -r option.
5. **groupadd -o -g 505 redhat** - For allocating a non-unique GID to a group, -o option is used .
6. **groupadd -K GID\_MIN=700 redhat** - The default values for login are defined in /etc/login.defs file. For overriding key-value pairs in this file, -K option is used.

**In groupmod command 80% options are same like groupadd.**
1. -n, --new-name NEW_GROUP<br/>
The name of the group will be changed from GROUP to NEW_GROUP name.
## userdel command
The userdel command modifies the system account files, deleting all entries that refer to login. The named user must exist.
<br/>
Some Examples:-
1. **userdel Salu** - To remove the user Salu account from the local system / server / workstation but it not delete it home directory .
2. **userdel -r Salu** - 
    * Files in the user's home directory will be removed along with the home directory itself and the user's mail spool. Files located in other file systems will have to be searched for and deleted manually.
    * The mail spool is defined by the MAIL_DIR variable in the login.defs file.
3. **userdel -f Salu**
    * This option forces the removal of the user account, even if the user is still logged in. It also forces userdel to remove the user's home directory and mail spool, even if another user uses the same home directory or if the mail spool is not owned by the specified user. If USERGROUPS_ENAB is defined to yes in /etc/login.defs and if a group exists with the same name as the deleted user, then this group will be removed, even if it is still the primary group of another user.

**Note: This option is dangerous and may leave your system in an inconsistent state.**

## groupdel command
The groupdel command modifies the system account files, deleting all entries that refer to GROUP. The named group must exist.
<br/>
Some Examples:-
1. **groupdel Salu** - To remove the group Redhat from the local system / server / workstation .

You may not remove the primary group of any existing user. You must remove the user before you remove the group.You should manually check all file systems to ensure that no files remain owned by this group.
<br/>
The groupdel command exits with the following values:
* 0 : - success
* 2 :- invalid command syntax
* 6 :- specified group doesn't exist
* 8 :- can't remove user's primary group
* 10 :- can't update group file

