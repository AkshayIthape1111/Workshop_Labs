# Access Command Line 
### Understanding the Shell
A commandline is a text based interface which can be used to input instruction to a computer system. The Linux commandline is provide a program called **shell**.
```
echo "hello"
echo $SHELL
```
How to see the environment variables
```
printenv
```
When the shell is used interactively,it displays a string when it is waiting for a command from the user.This is called **shell prompt**.<br/>
When the regular user starts a shell,the default prompt ends with a **$** character.
```
akshay-devops@1mp3r1sh4bl3:~$
```
* **akshay-devops** is my username 
  ```
  whoami
  ```
* **1mp3r1sh4bl3** is my hostname
  ```
  hostname
  ```
* **~** is my home directory 
  ```
  pwd
  ```
* **$** is for regular user<br/>
---
```
su -
```
When the **superuser(root)** user starts a shell,the default prompt ends with a **#** character.
```
root@1mp3r1sh4bl3:~#
```
* **root** is my username
  ```
  whoami
  ```
* **1mp3r1sh4bl3** is my hostname
  ```
  hostname
  ```
* **~** is my home directory 
  ```
  pwd
  ```
* **#** is for superuser user <br/>
---
### Shell Basics
Commands entered at shell prompt have three basic parts
* **Command to run**
* **Options to adjust the behavior of the command**
* **Arguments, which are typically targets of the command**
Examples
```
echo -e "hello \nhiiii \nhow are you" > akki
cat akki
cat -n akki
```
