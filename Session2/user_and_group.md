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
id
```
