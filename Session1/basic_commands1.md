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
### 3. ls command
---
ls - list directory contents and ls command is one of the most frequently used command in Linux. I believe ls command is the first command you may use when you get into the command prompt of Linux Box.
```
ls
ls -a
ls -la
ll
ls -lha
ls -ld /
ls -ltr  
```
Some Task for you 
1. See the content of / directory 
2. See all files of / directory
3. See the output in long listing format
4. I just want to see last modify directory
---
### vi command
---
VI editor is default file editor in linux system 
1. Vi stands for visual.
2. Vi have it’s variants like vim which stands for Vi IMproved, VimX11 for gui and winvi for MS windows.
3. Vi is the most popular editor and next most popular editor is gedit.
4. Do you know there is a book on VI editor from orally which is of 600+ pages.
5. Some other editors which will do the work of editing files are nano, pico, gedit, emacs, joe, nedit, ed etc
#### Modes of VI :-
Vi have two mode of operation.
1. Command mode : <br/>
Vi editor begins in command mode, where cursor movement(navigation in the file) and editing occur. To enter in to command mode from Inserting mode press esc button.<br/>
2. Inserting mode : <br/>
Used for entering text, this is similar to notepad in Windows. To enter in to inserting mode you can use any of the following.
```
i or I => Insert Mode
Esc => Command mode
: => Is used for give the command
w => Save in that file
q => Exit the editor
set nu => Is used for Set the numbers for Line 
wq => save and quit
w! => force save the file
q! => force quit without save
wq => save and quit forcefully
```
Some Task for you
1. Create file with vi editor and file name is exam.txt
2. Go to insert mode
3. Write "hello world" in that file 
4. Go to command mode 
5. Save that file 
6. Exit the editor
7. Open That file 
8. And set number to lines 
9. Exit the file
---
### 5. cat command
---
The cat command is one of the most frequently used command in Linux/Unix like operating systems. cat command allows us to create single or multiple files, view contain of file, concatenate files and redirect output in terminal or files.
```
cat exam.txt
cat > demo.txt
cat exam.txt > exam1.txt
cat exam.txt exam1.txt demo.txt
cat demo.txt exam.txt > final.txt
cat -n final.txt
cat exam.txt >> demo.txt 
cat < demo.txt
```
Some Task for you
1. Write the 'hello pune' in the file pune.txt
2. Write the 'hello sinhgad' in the file sinhgad.txt
3. I want diplay the sinhgad.txt and pune.txt using single command 
4. Redirect above command output to sinhgadpune.txt
5. Print the sinhgadpune.txt with line numbers
---
### 7. mkdir command
---
Short for "make directory", mkdir is used to create directories on a file system .<br/>
Some Examples :-
1. **mkdir akki** - It create akki directory in your current directory .
2. **mkdir -vp akshay**
   * -p no error if existing, make parent directories as needed
   * -v print a message for each created directory
3. **mkdir -m a=rwx akki OR mkdir -m 777 akki** - Create the akki directory, and set its permissions such that all users may read, write, and execute the contents

Some Task for you
1. Create directory 'pune/sinhgad' in / directory 
---
### 8. cp command
---
cp  command is used for copy files and directories <br/>
Some Examples :-
1. **cp main.c bak** - Copy single file main.c to destination directory bak
2. **cp main.c def.h /home/usr/rapid/** - Copy 2 files main.c and def.h to destination absolute path directory /home/usr/rapid/
3. **cp \*.c bak** - Copy all C files in current directory to subdirectory bak
4. **cp src /home/usr/rapid/** - Copy directory src to absolute path directory /home/usr/rapid/
5. **cp -R dev bak** - Copy all files and directories in dev recursively to subdirectory bak
6. **cp -f test.c bak** - Force file copy
7. **cp -i test.c bak** - Interactive prompt before file overwrite
8. **cp -u * bak** - Update all files in current directory - copy only newer files to destination directory bak

Some Task for you 
1. Copy file sinhgadpune.txt to '/pune/sinhgad' directory
2. Copy all contents of '/var/log' directory to '/pune/sinhgad' directory 
---
### 9. mv command
---
mv command is used to move files and directories.<br/>
Some Examples:-
1. **mv main.c def.h /home/usr/rapid/** - Move main.c def.h files to /home/usr/rapid/ directory
2. **mv \*.c bak** - Move all C files in current directory to subdirectory bak
3. **mv bak/\* .** - Move all files in subdirectory bak to current directory
4. **mv main.c main.bak** - Rename file main.c to main.bak
5. **mv bak bak2** - Rename directory bak to bak2
6. **mv -u main.c bak** - Update - move when main.c is newer
7. **mv -v main.c bak** - Move main.c and prompt before overwrite bak/main.c

Some Task for you 
1. Move all the contents of '/pune/sinhgad' directory to '/tmp' directory.
---
### 10. rm command
---
rm stands for ‘remove‘ as the name suggests rm command is used to delete or remove files and directory in UNIX like operating system. If you are new to Linux then you should be very careful while running rm command because once you delete the files then you can not recover the contents of files and directory. Though there are some tools and commands through which deleted files can be recovered but for that you need expert skills.<br/>
Some Examples:-
1. **rm linux.log** - Remove or delete a file.
2. **rm -i linuxstufff.log** - Delete the files interactively.
3. **rm -d appdata/** - Delete a empty directory
4. **rm -r dbstore/** - Deleting a directory recursively using ‘-r’ option
5. **rm -ri dbstore/** - Delete the files and sub-directories interactively.
6. **rm -f tech.txt** - Deleting files forcefully using ‘-f’ option
7. **rm -I linux_store/app\*** - Prompt once before deleting more than three files or recursive delete.
8. **rm -f log{1..5}.txt** - Regular expression in rm command .
9. **rm ./\ -store** - Delete a file which starts with hyphen symbol (-)

Some Task for you 
1. Remove all the contents of '/tmp' directory 
---
### 11. rmdir command
---
Short for "remove directory", rmdir is used to remove directories on a file system .<br/>
ext4_rmdir() system call attempts to remove a directory using pathname.
1. **rmdir akki** - It remove akki directory into your current directory if it is empty .
2. **rmdir -vp** - Remove DIRECTORY and its ancestors; e.g., 'rmdir -p a/b/c' is similar to 'rmdir a/b/c a/b a'

Some Task for you 
1. Remove the directory '/pune/sinhgad'
---
### 12. history command
---
We use history command frequently in our daily routine jobs to check history of command or to get info about command executed by user. <br/>
we will see how we can use history command effectively to extract the command which was executed by users in Bash shell. This may be useful for audit purpose or to find out what command is executed at what date and time. <br/>
Some Examples:-
1. **history** -  List Last/All Executed Commands in Linux
2. **history 3** - Print ‘n’ Lines
3. **!!** - Repeat Most Recent Command
4. **!101** - Repeat Specific Command 
5. **!systemctl** - Repeat Command Starting With A String
6. **history | grep httpd** - Piping History
7. **history -w** - Write To History File 
8. **history -c** - Clear History File

Some Task for you
1. Save the history to file 'history.txt' 
2. Clear the history 
---
