# Managing local linux users and groups 
## id command
---
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
---
## useradd command 
---
### Lab-1
```
useradd user1
passwd user1
su - user1
```
### Lab-2
```
useradd -m user2
passwd user2
su - user2
```
### Lab-3
```
useradd -s /sbin/nologin user3
passwd user3
su - user3
```
### Lab-4
```
useradd -m user4
cat /etc/passwd
cat /etc/shadow
```
---
## groupadd command
---
### Lab-1
```
groupadd linux_lab
```
### Lab-2
```
groupadd -g 3000 linux_lab1
cat /etc/group
cat /etc/gshadow
```
---
## usermod command
---
Lab-1
```
mkdir /user1
chown user1:user1 /user1
usermod -d /user1 user1
cat /etc/passwd 
su - user1
pwd
```
Lab-2
```
usermod -s /bin/bash user3
cat /etc/passwd
su - user3
```
Lab-3
```
usermod -glinux_lab user1
cat /etc/passwd
su - user1
id
```
Lab-4
```
usermod -Glinux_lab1 user2 
cat /etc/passwd
su - user2
id
```
---
## groupmod command
---
Lab-1
```
groupmod -n linux_lab linux_os
```
---
## userdel command
---
Lab-1
```
userdel user1
cat /etc/passwd
```
Lab-2
```
userdel -r user2
cat /etc/passwd
```
Lab-3
```
userdel -f user3
cat /etc/passwd
userdel user4
cat /etc/passwd
```
---
## groupdel command
---
Lab-1
```
groupdel linux_lab
groupdel linux_lab1
cat /etc/groups
```
---
# Thank You
