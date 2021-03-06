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
1. The /dev directory is the location of special or device files.
2. These include terminal devices, usb, or any device attached to the system.
3. See **/dev** directory by using following commands
   ```
   cd /dev
   ls -la
   ```
### /etc - Host-specific system configuration
---
1. The /etc hierarchy contains configuration files. A "configuration file" is a local file used to control the operation of a program; it must be static and cannot be an executable binary.
2. This also contains startup and shutdown shell scripts used to start/stop individual programs.
3. It is recommended that files be stored in subdirectories of /etc rather than directly in /etc.
4. See **/etc** directory by using following commands
   ```
   cd /etc
   ls -la
   ```
### /home - User home directories
---
1. Home directories for all users to store their personal files.
2. For example: /home/john, /home/nikita
3. See **/home** directory by using following commands
   ```
   cd /home
   ls -la
   ```
### /lib - Essential shared libraries and kernel modules
---
1. The /lib directory contains those shared library images needed to boot the system and run the commands in the root filesystem, ie. by binaries in /bin and /sbin.
2. See **/lib** directory by using following commands
   ```
   cd /lib
   ls -la
   ```
### /lib64 - Alternate format essential shared libraries
---
1. The /lib64 directory contains those shared library images needed to boot the system and run the commands in the root filesystem, ie. by binaries in /bin and /sbin.
2. See **/lib64** directory by using following commands
   ```
   cd /lib64
   ls -la
   ```
### /lost+found - Recover files 
---
1. Linux should always go through a proper shutdown. Sometimes your system might crash or a power failure might take the machine down. Either way, at the next boot, a lengthy filesystem check (the speed of this check is dependent on the type of filesystem that you actually use. ie. ext3 is faster than ext2 because it is a journalled filesystem) using fsck will be done. Fsck will go through the system and try to recover any corrupt files that it finds. The result of this recovery operation will be placed in this directory. The files recovered are not likely to be complete or make much sense but there always is a chance that something worthwhile is recovered. Each partition has its own lost+found directory. If you find files in there, try to move them back to their original location. If you find something like a broken symbolic link to 'file', you have to reinstall the file/s from the corresponding RPM, since your file system got damaged so badly that the files were mutilated beyond recognition. Below is an example of a /lost+found directory. As you can see, the vast majority of files contained here are in actual fact sockets. As for the rest of the other files they were found to be damaged system files and personal files. These files were not able to be recovered. 
### /media - Mount point for removable media
---
1. This directory contains subdirectories which are used as mount points for removable media such as floppydisks, USB,  cdroms and zip disks.
2. See **/media** directory by using following commands
   ```
   cd /media
   ls -la
   ```
### /mnt - Mount point for mounting a filesystem temporarily
---
1. Temporary mount directory where sysadmins can mount filesystems.
2. See **/mnt** directory by using following commands
   ```
   cd /mnt
   ls -la
   ```
### /opt - Add-on application software packages
---
1. /opt is reserved for the installation of add-on application software packages.
2. See **/opt** directory by using following commands
   ```
   cd /opt
   ls -la
   ```
### /proc - Kernel and process information virtual filesystem 
---
1. Contains information about system process.
2. This is a pseudo filesystem contains information about running process. For example: /proc/{pid} directory contains information about the process with that particular pid.
3. This is a virtual filesystem with text information about system resources. For example: /proc/uptime
4. See **/proc** directory by using following commands
   ```
   cd /proc
   ls -la
   ```
### /root - Home directory for the root user
---
1. Home directory for the root user so only root can access this directory. 
2. See **/root** directory by using following commands
   ```
   cd /root
   ls -la
   ```
### /run - Data relevant to running processes
---
1. This directory contains system information data describing the system since it was booted. Files under this directory must be cleared (removed or truncated as appropriate) at the beginning of the boot process.
2. The purposes of this directory were once served by /var/run. In general, programs may continue to use /var/run to fulfill the requirements set out for /run for the purposes of backwards compatibility. Programs which have migrated to use /run should cease their usage of /var/run, except as noted in the section on /var/run.
3. See **/run** directory by using following commands
   ```
   cd /run
   ls 
   ```
### /sbin - Essential system binaries
---
1. Utilities used for system administration (and other root-only commands) are stored in /sbin, /usr/sbin, and /usr/local/sbin. 
2. /sbin contains binaries essential for booting, restoring, recovering, and/or repairing the system in addition to the binaries in /bin. 
3. Programs executed after /usr is known to be mounted (when there are no problems) are generally placed into /usr/sbin. Locally-installed system administration programs should be placed into /usr/local/sbin.
4. There must be no subdirectories in /sbin.
5. See **/sbin** directory by using following commands
   ```
   cd /sbin
   ls -la
   ```
### /srv - Data for services provided by this system
---
1. /srv contains site-specific data which is served by this system.
2. See **/srv** directory by using following commands
   ```
   cd /srv
   ls -la
   ```
### /sys - Kernel and system information virtual filesystem
---
1. The sys filesystem is the location where information about devices, drivers, and some kernel features is exposed.
2. See **/sys** directory by using following commands
   ```
   cd /sys
   ls -la
   ```
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
