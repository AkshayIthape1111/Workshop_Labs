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
1. **ls** - ls with no option list files and directories in bare format where we won’t be able to view details like file types, size, modified date and time, permission and links etc.
2. **ls -l** - Shows file or directory, size, modified date and time, file or folder name and owner of file and it’s permission.
3. **ls -a** - List all files including hidden file starting with ‘.‘
4. **ls -lh** - With combination of -lh option, shows sizes in human readable format.
5. **ls -F** - Using -F option with ls command, will add the ‘/’ Character at the end each directory.
6. **ls -r** - The following command with ls -r option display files and directories in reverse order.
7. **ls -R** - Recursively list Sub-Directories .
8. **ls -ltr** - With combination of -ltr will shows latest modification file or directory date as last.
9. **ls -lS** - With combination of -lS displays file size in order, will display big in size first.
10. **ls -i** - We can see some number printed before file / directory name. With -i options list file / directory with inode number.
11. **ls -l /tmp** - With ls -l command list files under directory /tmp. Wherein with -ld parameters displays information of /tmp directory.
12. **ls -n** - To display UID and GID of files and directories. use option -n with ls command.
13. **ls -A** - do not list implied . and ..
14. **ls -d** - list directories themselves, not their contents
15. **ls -s** - print the allocated size of each file, in blocks
16. **ls -t** - sort by modification time, newest first
17. **ls -1** - list one file per line.
### vi command
---
VI editor is the default file editor in most of the Linux/Nix machines. It is having great capabilities to edit a file with in few key strokes.<br/>
Lets start with some general information and then move on to some good things what vi editor can do for you while editing a file.
1. Vi stands for visual.
2. Vi have it’s variants like vim which stands for Vi IMproved, VimX11 for gui and winvi for MS windows.
3. Vi is the most popular editor and next most popular editor is gedit.
4. Do you know there is a book on VI editor from orally which is of 600+ pages.
5. Some other editors which will do the work of editing files are neno, pico, gedit, emacs, joe, nedit, ed etc.<br/>
Learning vi editor and remembering them is a very a easy task if you learn it in a systematic way.
* Modes of VI
* Navigational commands
* Editing commands.
* Search and Replace
* Save and quiting a file.
#### Modes of VI :-
Vi have two mode of operation.
1. Command mode
2. Inserting mode<br/>
Command mode : <br/>
Vi editor begins in command mode, where cursor movement(navigation in the file) and editing occur. To enter in to command mode from Inserting mode press esc button.<br/>
Inserting mode : <br/>
Used for entering text, this is similar to notepad in Windows. To enter in to inserting mode you can use any of the following.
```
i or I => present line
o => one line down the present line
O => one line above
Note : All comments will work in command mode only.
```
#### Navigational commands :-
1. Character navigation k, h, l and j
```
h => To move one character left.
j => To move one line down.
k => To move one line up.
l => To move one character right.
How to use above commands in clever way?
Examples :
6j => to move 6 lines down from the present courser.
7k => to move 7 lines above from the present courser.
```
2. Word Navigation
```
w => word forward.
e =>word forward, but end of the word.
b => one word backward.
Examples :
32w => To move 32 words forward
6b => To move 6 words back.
```
3. Setting numbering to lines
```
:set nu
Removing of nummbering to lines
:set nonu
```
4. Moving paragraphs
```
move one paragraph up => {{
move one paragraph down => }}
```
5. Moving page up/down
```
For up => ctrl+b
For down => ctrl+f
```
6. Moving start/end of the file
```
Starting of the file(first line => [[
End of the file(last line) => ]]
```
7. Going to any line :
```
:lineno
Example :
If we want to go to 56 line then type
:56
```
#### Editing commands :-
8. Replace one letter
```
Replace one letter => r
Delete one letter => x
```
9. Editing one word
```
Edit one word => cw
Delete one word => dw
```
10. Editing one line
```
Editing a line from courser to the end of that line => d$
```
11. Cutting
```
deleting(cutting) one line => dd
Examples :
2dd(deleting/cutting two lines)
```
12. Pasting
```
Pasting a line below the courser => p
Pasting a line above the courser => P
```
13. Coping
```
Copying one line => yy
Copying n lines => nyy
```
14. Special commands
```
joining lines => J
undoing things => u
repeating the previous command => .
```
#### Search and replace :-
15. Search for a term /term
```
Example : If you want to search for suresh then press /suresh enter
/suresh
Moving to next occurrence, press “n” without quotes moving to the previous occurrence, press “N” without quotes.
```
16. Searching and replacing a term(here separator is / )
```
:%s/searchterm/replaceterm/g
change default separator
:%s_/home/surya/grade_/home/testing/dest_g
```
17. To search and replace particular term from given line to other given line.
```
:%s294,304/sahana/xyz/g
```
#### Save and quiting a file :-
```
:w => save the file
:q => quit the file
:wq => save and quit
:w! => force save the file
:q! => force quit without save
:wq => save and quit forcefully
```
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
