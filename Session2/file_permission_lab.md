# File Permission 

## Prerequisite
1. Create user 'user1' and 'user2' with home directory .
2. Create the file 'user1.txt' in user1 home directory .
3. Create the directory 'hello' in user2 home directory and create file 'user2.txt' in that directory.

## View The Permission
---
1. to view permissions of a regular file
```
ls -l /home/user1/user1.txt
ls -la /home/user2/hello/user2.txt
```
2. to view permissions of a directory
```
ls -ld /home/user2/hello
```
---
## Change the permission 
---
Lab-1(user1.txt is should not be read by user 'user2' )
```
su - user2
cd /home/user1/
cat user1.txt
exit
================================
su - user1
ll user1.txt
chmod 770 user1.txt OR chmod o-r user1.txt
ll user1.txt
exit
================================
su - user2
cd /home/user1/
cat user1.txt
exit 
```
Lab-2(user 'user1' should not be able to go to the directory 'user2/hello')
```
su - user1
cd /home/user2/hello/
ls
exit
================================
su - user2
ll
chmod 770 hello OR chmod o-rx hello
ll
exit
================================
```
Lab-3(user1.txt is should be read and write by user 'user2')
```
do it yourself
```
Lab-4(user 'user1' should be able to go to the directory 'user2/hello' and he should be able to create directory on that directory)
```
do it yourself
```
---
## Change the default permission 
---
Lab-1
```
touch akki
mkdir akki1
ll 
umask
```
Lab-2
```
umask 0007
umask
touch king
mkdir king1
ll
```
---
## Change the Owner of the file 
Lab-1(Change the owner of the file 'user1.txt' to user 'user2')
```
su - user1
chown user2:user2 user1.txt
ll user1.txt
```
Lab-2(change the owner of the directory 'user2/hello' to user 'user1')
```
do it yourself
```
---
