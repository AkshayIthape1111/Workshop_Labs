# Multi Ways To Login Into System
## Graphical Login
* Everyone should know about this step of login and everyone is used this . 
## Virtual Console Login
* Ctrl+Alt+F1 to F7 any key
* F7 is for graphical console 
## Remote Login
* ssh :- <br/>
  The SSH protocol (also referred to as Secure Shell) is a method for secure remote login from one computer to another.
  ```
  tty
  ssh akshay-devops@localhost
  tty
  ```
* telnet :- <br/>
  The telnet command is used to communicate with another host using the TELNET protocol. If telnet is invoked without the host argument, it enters command mode, indicated by its prompt (telnet>).
  ```
  telnet
  ```
* ftp/sftp :- <br/>
  File Transfer Protocol (FTP) was widely used protocol to transfer files or data remotely in unencrypted format which is not secure way to communicate. As we all know that File Transfer Protocol is not at all secure because all transmissions happens in clear text and the data can be readable by anyone during sniffing the packets on the network.
  SFTP (Secure File Transfer Protocol) runs over SSH protocol on standard port 22 by default to establish a secure connection. SFTP has been integrated into many GUI tools (FileZilla, WinSCP, FireFTP etc.).
  ```
  sftp akshay-devops@localhost
  ```
