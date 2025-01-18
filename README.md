# Learn CLI Linux

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/3/35/Tux.svg" alt="Linux Logo" width="120" height="120">
</p>

This documentation provides a comprehensive list of essential Linux commands, categorized for clarity and ease of reference. Whether you are new to Linux or an experienced user, this guide serves as a practical resource to improve your command-line skills.

Contributions are encouraged. If you would like to suggest additional commands or improvements, please submit a pull request.

---

## Table of Contents

1. [Introduction](#introduction)  
2. [File and Directory Management](#file-and-directory-management)  
3. [Viewing and Editing Files](#viewing-and-editing-files)  
4. [User and Permission Management](#user-and-permission-management)  
5. [Process and System Management](#process-and-system-management)  
6. [Networking Tools](#networking-tools)  
7. [Package Management](#package-management)  
8. [Compression and Archiving](#compression-and-archiving)  
9. [Disk and Filesystem Management](#disk-and-filesystem-management)  
10. [Miscellaneous Commands](#miscellaneous-commands)  
11. [Contributing](#contributing)  

---

## 1. Introduction

Linux is a versatile operating system widely used for development, server management, and system administration. Mastering the Linux command line interface (CLI) is essential for effective system operation and troubleshooting.  

This documentation categorizes the most commonly used commands to help you navigate and use the Linux CLI efficiently.

---

<details>
<summary>📂 <strong>2. File and Directory Management</strong></summary>

### Navigation
- **`ls`** - List files and directories.  
  Example: `ls -la /var/www/html`  
- **`cd`** - Change the current directory.  
  Example: `cd /home/user/Documents`  
- **`pwd`** - Display the current working directory.  
  Example: Output: `/home/user/Projects`

### Creation and Deletion
- **`mkdir`** - Create a new directory.  
  Example: `mkdir /home/user/Backup`  
- **`rmdir`** - Remove an empty directory.  
  Example: `rmdir /home/user/OldFolder`  
- **`rm`** - Delete files or directories.  
  Example: `rm -r /home/user/TempFiles`  

### File Operations
- **`cp`** - Copy files or directories.  
  Example: `cp /etc/nginx/nginx.conf /home/user/nginx_backup.conf`  
- **`mv`** - Move or rename files/directories.  
  Example: `mv /home/user/file.txt /home/user/Documents/file_renamed.txt`

### Searching
- **`find`** - Search for files or directories.  
  Example: `find /home/user -name "report.pdf"`  
- **`locate`** - Quickly locate files.  
  Example: `locate settings.json`  

</details>

---

<details>
<summary>📂 <strong>3. Viewing and Editing Files</strong></summary>

- **`cat`** - Display the content of a file.  
  Example: `cat /etc/hosts`  
- **`less`** - View file content one page at a time.  
  Example: `less /var/log/syslog`  
- **`head`** - Show the first few lines of a file.  
  Example: `head -n 5 /var/log/auth.log`  
- **`tail`** - Show the last few lines of a file.  
  Example: `tail -f /var/log/apache2/access.log` (for live monitoring).  
- **`nano`** - Edit files in a simple text editor.  
  Example: `nano /etc/fstab`  
- **`vim`** - Advanced text editor for editing files.  
  Example: `vim /home/user/.bashrc`  
- **`sed`** - Stream editor for modifying file content.  
  Example: `sed 's/old-word/new-word/g' /home/user/document.txt`  

</details>

---

<details>
<summary>📂 <strong>4. User and Permission Management</strong></summary>

### User Management
- **`whoami`** - Display the current user.  
  Example: Output: `user`  
- **`id`** - Show user ID and group information.  
  Example: `id user`  
- **`adduser`** - Add a new user.  
  Example: `sudo adduser new_user`  
- **`passwd`** - Change a user password.  
  Example: `sudo passwd new_user`  
- **`su`** - Switch to another user or root.  
  Example: `su root`  

### Permission Management
- **`chmod`** - Change file or directory permissions.  
  Example: `chmod 644 /var/www/html/index.html`  
- **`chown`** - Change file ownership.  
  Example: `chown user:user /home/user/project`  

</details>

---

<details>
<summary>📂 <strong>5. Process and System Management</strong></summary>

### Process Management
- **`ps`** - Display running processes.  
  Example: `ps aux | grep nginx`  
- **`top`** / **`htop`** - Monitor processes in real-time.  
- **`kill`** - Terminate a process by its PID.  
  Example: `kill 1234`  
- **`killall`** - Terminate all processes with a specific name.  
  Example: `killall nginx`  

### System Monitoring
- **`uptime`** - Show system uptime and load.  
- **`df`** - Display available disk space.  
  Example: `df -h /dev/sda1`  
- **`du`** - Display directory or file sizes.  
  Example: `du -sh /home/user/Projects`  

</details>

---

<details>
<summary>📂 <strong>6. Networking Tools</strong></summary>

- **`ping`** - Check connectivity to a host.  
  Example: `ping 8.8.8.8`  
- **`curl`** - Fetch data from a URL.  
  Example: `curl https://example.com/api/status`  
- **`wget`** - Download files from a URL.  
  Example: `wget https://example.com/file.zip`  
- **`ifconfig`** / **`ip a`** - Display network interface information.  
- **`ssh`** - Connect to a remote server securely.  
  Example: `ssh user@192.168.1.10`  

</details>

---

<details>
<summary>📂 <strong>7. Package Management</strong></summary>

### Debian/Ubuntu (APT)
- **`apt update`** - Refresh package lists.  
- **`apt upgrade`** - Upgrade all installed packages.  
- **`apt install`** - Install a specific package.  
  Example: `sudo apt install git`  
- **`apt remove`** - Remove an installed package.  
  Example: `sudo apt remove apache2`  

### Fedora/RedHat (DNF)
- **`dnf update`** - Update installed packages.  
- **`dnf install`** - Install a package.  
  Example: `sudo dnf install httpd`  
- **`dnf remove`** - Remove a package.  
  Example: `sudo dnf remove php`  

</details>

---

<details>
<summary>📂 <strong>8. Compression and Archiving</strong></summary>

- **`tar`** - Create/extract tar archives.  
  Example: `tar -czvf backup.tar.gz /home/user/Projects`  
- **`gzip`** - Compress files.  
  Example: `gzip /home/user/report.txt`  
- **`unzip`** - Extract ZIP files.  
  Example: `unzip /home/user/archive.zip`  

</details>

---

<details>
<summary>📂 <strong>9. Disk and Filesystem Management</strong></summary>

- **`mount`** - Mount a filesystem.  
  Example: `sudo mount /dev/sdb1 /mnt/external_drive`  
- **`umount`** - Unmount a filesystem.  
  Example: `sudo umount /mnt/external_drive`  
- **`fdisk`** - Partition management.  
  Example: `sudo fdisk /dev/sda`  
- **`mkfs`** - Format a partition with a filesystem.  
  Example: `mkfs.ext4 /dev/sdb1`  

</details>

---

<details>
<summary>📂 <strong>10. Miscellaneous Commands</strong></summary>

- **`alias`** - Create command shortcuts.  
  Example: `alias ll='ls -la'`  
- **`echo`** - Print text to the terminal.  
  Example: `echo "Hello, world!"`  
- **`date`** - Display the current date and time.  
  Example: `date "+%Y-%m-%d %H:%M:%S"`  
- **`history`** - View command history.  
  Example: `history | grep ssh`  
- **`clear`** - Clear the terminal screen.  

</details>

---

## 11. Contributing

Contributions are welcome. If you have additional commands to suggest or improvements to propose:  
1. Fork this repository.  
2. Make your changes.  
3. Submit a pull request with a clear description.  

