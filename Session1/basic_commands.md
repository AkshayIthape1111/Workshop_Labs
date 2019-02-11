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
---
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
---
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
---
### vi command
---
VI editor is the default file editor in most of the Linux/Nix machines. It is having great capabilities to edit a file with in few key strokes.<br/>
Lets start with some general information and then move on to some good things what vi editor can do for you while editing a file.
1. Vi stands for visual.
2. Vi have it’s variants like vim which stands for Vi IMproved, VimX11 for gui and winvi for MS windows.
3. Vi is the most popular editor and next most popular editor is gedit.
4. Do you know there is a book on VI editor from orally which is of 600+ pages.
5. Some other editors which will do the work of editing files are neno, pico, gedit, emacs, joe, nedit, ed etc.

Learning vi editor and remembering them is a very a easy task if you learn it in a systematic way.
* Modes of VI
* Navigational commands
* Editing commands.
* Search and Replace
* Save and quiting a file.
#### Modes of VI :-
Vi have two mode of operation.
1. Command mode : <br/>
Vi editor begins in command mode, where cursor movement(navigation in the file) and editing occur. To enter in to command mode from Inserting mode press esc button.<br/>
2. Inserting mode : <br/>
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
---
### cat command
---
The cat command is one of the most frequently used command in Linux/Unix like operating systems. cat command allows us to create single or multiple files, view contain of file, concatenate files and redirect output in terminal or files.
<br/>
Some Examples:-
1. **cat a.txt** - It print a.txt file on terminal .
2. **cat a.txt b.txt** - It print 1st a.txt file after that he print b.txt file on CLI
3. **cat >  king.txt** - Awaits input from user, type desired text and press CTRL+D (hold down Ctrl Key and type ‘d‘) to exit. The text will be written in king file
4. **cat tp1.txt | more OR cat tp2.txt | less** - If file having large number of content that won’t fit in output terminal and screen scrolls up very fast, we can use parameters more and less with cat command as show above.
5. **cat -n tp1.txt** - With -n option you could see the line numbers of a file tp1.txt in the output terminal.
6. **cat -e test.txt** - you can see with -e option that ‘$‘ is shows at the end of line and also in space showing ‘$‘ if there is any gap between paragraphs. This options is useful to squeeze multiple lines in a single line.
7. **cat -T test.txt** - we could see TAB space is filled up with ‘^I‘ character.
8. **cat test > test1** - We can redirect standard output of a file into a new file else existing file with ‘>‘ (greater than) symbol. Careful, existing contents of test1 will be overwritten by contents of test file.
9. **cat test >> test1** - Appends in existing file with ‘>>‘ (double greater than) symbol. Here, contents of test file will be appended at the end of test1 file.
10. **cat < test2** - When you use the redirect with standard input ‘<‘ (less than symbol), it use file name test2 as a input for a command and output will be shown in a terminal.
---
### stat command
---
stat command is a useful utility for viewing file or file system status. It retrieves information such as file type; access rights in octal and human-readable; SELinux security context string; time of file birth, last access, last data modification, last status change in both human-readable and in seconds since Epoch, and much more.<br/>
It has an option to specify a custom format instead of the default, for displaying information.<br/>
Some Examples:-
1. **stat /var/log/syslog** - This command will display the size, blocks, IO blocks, file type, inode value, number of links and much more information about the file /var/log/syslog
2. **stat -f /var/log/syslog** - stat command treated the input file as a normal file, however, to display file system status instead of file status, use the **-f** option.
3. **stat -L /** - Since Linux supports links (symbolic and hard links), certain files may have one or more links, or they could even exist in a filesystem.To enable stat to follow links, use the -L flag
4. **stat --printf='%U\n%G\n%C\n%z\n' /var/log/secure** - Use a Custom Format To Display Information
   * %U – user name of owner
   * %G – group name of owner
   * %C – SELinux security context string
   * %z – time of last status change, human-readable
5. **stat -t /var/log/syslog** - The **-t** option can be used to print the information in terse form.
---
### mkdir command
---
Short for "make directory", mkdir is used to create directories on a file system .<br/>
ext4_mkdir() system call attempts to create a directory named pathname.<br/>
On older kernels where mkdirat() is unavailable, the glibc wrapper function falls back to the use of mkdir().  When  pathname  is  a relative pathname, glibc constructs a pathname based on the symbolic link in /proc/self/fd that corresponds to the dirfd argument.<br/>
Some Examples :- 
1. **mkdir akki** - It create akki directory in your current directory .
2. **mkdir -vp**
   * -p no error if existing, make parent directories as needed 
   * -v print a message for each created directory
3. **mkdir -m a=rwx akki OR mkdir -m 777 akki** - Create the akki directory, and set its permissions such that all users may read, write, and execute the contents
---
### cp command
---
---
### mv command
---
---
### rm command
---
---
### rmdir command
---
Short for "remove directory", rmdir is used to remove directories on a file system .<br/>
ext4_rmdir() system call attempts to remove a directory using pathname.
1. **rmdir akki** - It remove akki directory into your current directory if it is empty .
2. **rmdir -vp** - Remove DIRECTORY and its ancestors; e.g., 'rmdir -p a/b/c' is similar to 'rmdir a/b/c a/b a'
---
### file command
---
The file command determines the file type of a file. It reports the file type in human readable format (e.g. ‘ASCII text’) or MIME type (e.g. ‘text/plain; charset=us-ascii’). As filenames in UNIX can be entirely independent of file type file can be a useful command to determine how to view or work with a file.<br/>
Some Examples:-
1. **file akki.txt** - To determine the file type of a file pass the name of a file to the file command.The file name along with the file type will be printed to standard output.
2. **file -b akki.txt** - To show just the file type pass the -b option. 
---
### head command
---
The head command reads the first few lines of any text given to it as an input and writes them to standard output (which, by default, is the display screen). <br/>
head, by default, prints the first 10 lines of each FILE to standard output. <br/>
Some Examples :- 
1. **head myfile.txt** - Display the first ten lines of myfile.txt.
2. **head -15 myfile.txt** - Display the first fifteen lines of myfile.txt.
3. **head myfile.txt myfile2.txt** - Display the first ten lines of both myfile.txt and myfile2.txt, with a header before each that indicates the file name.
4. **head -n 5 myfile.txt myfile2.txt** - Displays only the first 5 lines of both files.
5. **head -c 20 myfile.txt** - Displays the first 20 bytes of myfile.txt
6. **head -n 5K myfile.txt** - Displays the first 5,000 lines of myfile.txt.
7. **head -c 6M myfile.txt** - Displays the first six megabytes.
8. **head -** - If a dash is specified for the file name, head reads from standard input rather than a regular file.
9. **head -n 4 \*.txt** - Display the first four lines of every file in the working directory whose file name ends in the extension .txt.
10. **head -n 4 -q \*.txt** - Same as the previous command, but uses quiet (-q) output, which will not print a header before the lines of each file.
---
### tail command
The tail command reads the final few lines of any text given to it as an input and writes them to standard output (which, by default, is the monitor screen). <br/>
tail prints the last 10 lines of each FILE to standard <br/>
Some Examples :- 
1. **tail myfile.txt** - Outputs the last 10 lines of the file myfile.txt.
2. **tail -15 myfile.txt** - Display the last fifteen lines of myfile.txt.
3. **tail -f myfile.txt** - Outputs the last 10 lines of myfile.txt, and monitors myfile.txt for updates; tail then continues to output any new lines that are added to myfile.txt.
4. **tail -n 5 myfile.txt myfile2.txt** - Displays only the last 5 lines of both files.
5. **tail -c 20 myfile.txt** - Displays the last 20 bytes of the myfile.txt
6. **tail -n 5K myfile.txt** - Displays the last 5,000 lines of myfile.txt.
7. **tail -c 6M myfile.txt** - Displays the last six megabytes.
8. **tail -n 4 \*.txt** - Display the last four lines of every file in the working directory whose file name ends in the extension .txt.
---
### history command
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
---
