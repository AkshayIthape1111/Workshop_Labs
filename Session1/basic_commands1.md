# Basic Commands
1. There are a countless number of commands in Linux.
2. We are bound to use a number of them on a daily routine or numerous times to perform common tasks than others. 

### 1. echo command
---
'echo command' is display a line of text
```
echo "hello world"
echo -e "hello \nworld"
echo $SHELL
echo -e "#include<stdio.h>\nint main(){\nprintf(\"hello this is c program \");\nreturn 0;\n}" > akki.c
gcc akki.c
./a.out
```
#### Your Task 
1. Using echo command write the hello world c program
```
echo -e "#include<stdio.h>\nint main(){\nprintf(\"hello this is c program \");\nreturn 0;\n}" > akki.c
gcc akki.c
./a.out
```
---
### 2. pwd command
---
Print name of current/working directory . The getcwd() function copies an absolute pathname of the current working directory to the array pointed to by buf .
```
pwd
```
---
### 3. cd commad
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
---

