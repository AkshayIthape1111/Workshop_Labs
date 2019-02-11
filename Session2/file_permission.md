# File Permission in Linux
---
Linux is multi-user operating system which can be accessed by many users simultaneously. Linux can also be used in mainframes and servers without any modifications. But this raises security concerns as any user can corrupt, change or remove crucial data. <br/>
For effective security , Linux divides authorization into 2 levels
* Ownership
* Permission
## Ownership in Linux files
In every linux system there are 3 sets of people for whom we may specify permissions.
* User
Every file has only one owner and A user is the owner of the file. By default, the person who created a file becomes its owner. 
* Group
Every file belongs to a single group . group can contain multiple users. All users belonging to a group will have the same access permissions to the file. Suppose you have a project where a number of people require access to a file. Instead of manually assigning permissions to each user, you could add all users to a group, and assign group permission to file .
* Other
Everyone else who is not in the group or the owner when you set the permission for others, it is also referred as set permissions for world .
## Permission in Linux files
Every file and directory in your Linux system has read , write and execute permissions defined for user , group and Others by the owner of the file<br/>
“- (dash) specific permission has not been assigned”<br/>
We see one by one in Details :-
* Read 
This permission give you the authority to open and read a file. Read permission on a directory gives you the ability to lists it's content.
* Write
The right permission gives you the authority to modify the contents of a file. The write permission on a directory gives you the authority to add , remove and rename files stored in the directory. 
* Execute
In Unix/Linux , you cannot run a program unless the execute permission is set. If the execute permission is not set, you might still be able to see/modify the program code(provided read & write permissions are set), but not actually run it. In linux default not execute permission for every file .
