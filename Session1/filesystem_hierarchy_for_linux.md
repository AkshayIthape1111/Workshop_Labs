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
### /bin - Essential User Binaries
---
1. Contains binary executables files only.
2. There is no sub-directory in bin.
3. Common linux commands you need to use in single-user modes are located under this directory.
4. Commands used by all the regular users of the system are located here.
5. For example: bash,cat,echo,cp,mv,hostname,whoami and there are some many .
6. See **/bin** directory by using following commands
   ```
   cd /bin
   ls -la
   ```
### /boot - Static files of the boot loader
---
1. This directory contains the files which should needed to boot the system.
2. All booting related files are stored in this directory only.
3. Such as Kernel initrd (Initial RAM Disk image), vmlinuz (Virtual Memory LINUx gZip – compressed Linux kernel Executable) & grub (Grand Unified Bootloader). 
4. See **/boot** directory by using following commands
   ```
   cd /boot
   ls -la
   ``` 
### /cdrom - Historical Mount Point for CD-ROMs
---
1. This directory isn’t part of the FHS standard, but you’ll still find it on Ubuntu and other operating systems. It’s a temporary location for CD-ROMs inserted in the system. However, the standard location for temporary media is inside the /media directory.
2. See **/cdrom** directory by using following commands
   ```
   cd /cdrom
   ls -la
   ```
### /dev - Device files
---
### /etc - Host-specific system configuration
---
### /home - User home directories
---
### /lib - Essential shared libraries and kernel modules
---
### /lib64 - Alternate format essential shared libraries
---
### /lost+found - 
---
### /media - Mount point for removable media
---
### /mnt - Mount point for mounting a filesystem temporarily
---
### /opt - Add-on application software packages
---
### /proc - Kernel and process information virtual filesystem 
---
### /root - Home directory for the root user
---
### /run - Data relevant to running processes
---
### /sbin - Essential system binaries
---
### /snap - 
---
### /srv - Data for services provided by this system
---
### /sys - Kernel and system information virtual filesystem
---
### /tmp - Temporary files
---
1. Directory that contains temporary files created by system and users.
2. Files under this directory are deleted when system is rebooted.
3. See **/tmp** directory by using following commands
   ```
   cd /tmp
   ls -la
   ```
### /usr - Secondary hierarchy
---
1. /usr usually contains by far the largest share of data on a system. 
2. Hence, this is one of the most important directories in the system as it contains all the user binaries, their documentation, libraries, header files, etc.... X and its supporting libraries can be found here. User programs like telnet, ftp, etc.... are also placed here.
   ```
   /usr/
   ├── bin - Most user commands
   ├── games - Games and educational binaries 
   ├── include - Header files included by C programs
   ├── lib - Libraries
   ├── local - Local hierarchy (empty after main installation)
   ├── sbin - Non-vital system binaries
   ├── share - Architecture-independent data
   └── src - Source code 
   ```
3. See **/usr** directory by using following commands
   ```
   cd /usr
   ls -la
   ``` 
### /var - Variable data 
---
1. Variable files whose content is expected to continually change during normal operation of the system—such as logs, spool files, and temporary e-mail files. 
2. This includes system log files (/var/log); packages and database files (/var/lib); emails (/var/mail); print queues (/var/spool); lock files (/var/lock); temp files needed across reboots (/var/tmp);
3. See **/var** directory by using following commands
   ```
   cd /var
   ls -la
   ```
### /vmlinuz
---
1. Normally the kernel or symbolic link to the kernel.
### /initrd.img
---
1. initrd provides the capability to load a RAM disk by the bootloader.
2. initrd is mainly designed to allow system startup to occur in two phases, where the kernel comes up with a minimum set of compiled−in drivers, and where additional modules are loaded from initrd.
