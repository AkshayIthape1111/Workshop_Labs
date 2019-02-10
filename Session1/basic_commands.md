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
### ls command
---
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
