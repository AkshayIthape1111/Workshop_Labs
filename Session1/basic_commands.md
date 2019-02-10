# Basic Commands
There are a countless number of commands in Linux. We are bound to use a number of them on a daily routine or numerous times to perform common tasks than others. It is important to note that certain commands are “distro-based” – they can only be found in specific distros. While others are generic Unix/Linux commands that you’ll find in all if not most mainstream distros.
<br/>
Now we'll discus about some basic linux commands with examples, you're almost always going to need those commands, so better to remember them. 
### pwd command
---
Print name of current/working directory . The getcwd() function copies an absolute pathname of the current working directory to the array pointed to by buf .
```
pwd
```
### cd command
---
cd command is use for change current directory to other directory using absolute path or relative path .<br/>
There is no manual entry for cd (No man page of cd command) .<br/>
**Absolute path** - An absolute path is defined as the specifying the location of a file or directory from the root directory(/). In other words we can say absolute path is a complete path from start of actual filesystem from / directory.
<br/>
Example :-
   ```
   cd /home/akki
   ```
**Relative path** - Relative path is defined as path related to the present working directory(pwd). Suppose I am located in /var/log and I want to change directory to /var/log/kernel. I can use relative path concept to change directory to kernel
<br/>
Example :-
   ```
   cd kernel 
   ```
Some more examples for cd command
   ```
   cd ..       //It change current directory to parent directory 
   cd .        //The current directory it is represented by a single dot (".")
   cd or cd ~  //It change to home directory  
   
   ```
Some Task for you 
1. Change your working directory to root directory
2. Go to the log directory which is under var directory using relative path
3. Go to your home directory 
### ls command
---
ls - list directory contents and ls command is one of the most frequently used command in Linux. I believe ls command is the first command you may use when you get into the command prompt of Linux Box. 
<br/>
Some examples
1. ls - ls with no option list files and directories in bare format where we won’t be able to view details like file types, size, modified date and time, permission and links etc.
2. ls -l - Shows file or directory, size, modified date and time, file or folder name and owner of file and it’s permission.
3. ls -a - List all files including hidden file starting with ‘.‘
4. ls -lh - With combination of -lh option, shows sizes in human readable format.
5. ls -F - Using -F option with ls command, will add the ‘/’ Character at the end each directory.
6. ls -r - The following command with ls -r option display files and directories in reverse order.
7. ls -R - Recursively list Sub-Directories .
8. ls -ltr - With combination of -ltr will shows latest modification file or directory date as last.
9. ls -lS - With combination of -lS displays file size in order, will display big in size first.
10. ls -i - We can see some number printed before file / directory name. With -i options list file / directory with inode number.
11. ls -l /tmp - With ls -l command list files under directory /tmp. Wherein with -ld parameters displays information of /tmp directory.
12. ls -n - To display UID and GID of files and directories. use option -n with ls command.
13. ls -A - do not list implied . and ..
14. ls -d - list directories themselves, not their contents
15. ls -s - print the allocated size of each file, in blocks
16. ls -t - sort by modification time, newest first
17. ls -1 - list one file per line.
### vi/nano command
---
### cat command
---
### stat command
---
### mkdir command
---
### cp command
---
### mv command
---
### rm command
---
### rmdir command
---
### file command
---
### head/tail command
---
### history command
---
