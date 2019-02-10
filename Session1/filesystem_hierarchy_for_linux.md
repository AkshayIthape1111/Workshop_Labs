# Filesystem Hierarchy For Linux
All files on a linux system are stored on file systems which are organized into a single inverted tree of directories, known as a **file system hierarchy**.This tree is inverted because the root of the tree is said to be at the top of the hieratchy, and the branches of directories and subdirectories stretch below the root.
```
/
├── bin
├── boot
├── cdrom
├── dev
├── etc
├── home
├── initrd.img -> boot/initrd.img-4.4.0-31-generic
├── lib
├── lib64
├── lost+found
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── snap
├── srv
├── sys
├── tmp
├── usr
├── var
└── vmlinuz -> boot/vmlinuz-4.4.0-31-generic
```
### / - The Root Directory
---
1. Everything on your Linux system is located under the / directory, known as the **root directory**.
2. Only root user has write privilege under this directory. 
3. See **/** directory by using following commands   
   ```
   cd /
   ls -la
   ```
### bin - Essential User Binaries
---
1. Contains binary executables files only.
2. There is no sub-directory in bin.
3. Common linux commands you need to use in single-user modes are located under this directory.
4. Commands used by all the regular users of the system are located here.
5. For example: bash,cat,echo,cp,mv,hostname,whoami and there are some many .
### boot
---

### cdrom
---
### dev
---
### etc
---
### home
---
### lib
---
### lib64
---
### lost+found
---
### media
---
### mnt
---
### opt
---
### proc
---
### root
---
### run
---
### sbin
---
### snap
---
### srv
---
### sys
---
### tmp
---
### usr
---
### var
---
### vmlinz
---
### initrd.img
---
