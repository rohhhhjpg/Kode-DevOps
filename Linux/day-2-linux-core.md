■ Linux Core Concepts

■ Kernel Information Commands
| Command  | Usage                       | Example  |
| -------- | --------------------------- | -------- |
| uname    | Display system information  | uname    |
| uname -r | Show kernel version         | uname -r |
| uname -a | Show all system information | uname -a |

■ Working With Hardware Commands
| Command             | Usage                        | Example             |
| ------------------- | ---------------------------- | ------------------- |
| dmesg               | Display kernel boot messages | dmesg               |
| dmesg | grep -i usb | Filter USB related logs      | dmesg | grep -i usb |
| udevadm info        | Device manager information   | udevadm info        |
| udevadm monitor     | Monitor device events        | udevadm monitor     |
| lspci               | List PCI devices             | lspci               |
| lsblk               | List block devices           | lsblk               |
| lscpu               | Display CPU information      | lscpu               |
| lsmem --summary     | Show memory summary          | lsmem --summary     |
| free -m             | Show memory in MB            | free -m             |
| free -k             | Show memory in KB            | free -k             |
| free -g             | Show memory in GB            | free -g             |
| lshw                | Show hardware info           | lshw                |
| sudo lshw           | Show detailed hardware info  | sudo lshw           |

■ Linux Kernel Responsibilities

Linux Kernel responsible for:

* Memory Management
* Process Management
* Device Drivers
* System Calls and Security

■ Linux Kernel Version Structure

5.15.0-76-generic

Breakdown:

5 → Major Version
15 → Minor Version
0 → Patch Version

■ Linux Boot Sequence

Linux Boot Process has 4 Stages

| Stage                  | Description                        |
| ---------------------- | ---------------------------------- |
| BIOS POST              | Hardware initialization and checks |
| Boot Loader (GRUB2)    | Loads Linux Kernel                 |
| Kernel Initialization  | Kernel loads drivers and services  |
| INIT Process (systemd) | Starts system services             |

■ Commands

| Command                                 | Usage                   | Example                                 |
| --------------------------------------- | ----------------------- | --------------------------------------- |
| ls -l /sbin/init                        | Check init system used  | ls -l /sbin/init                        |
| systemctl get-default                   | Show default runlevel   | systemctl get-default                   |
| systemctl set-default multi-user.target | Change default runlevel | systemctl set-default multi-user.target |


■ Systemd Targets (Runlevels)

Runlevels were used in SysV init systems
Now replaced by systemd targets

■ Complete Runlevels Mapping

| Runlevel | Systemd Target    | Description      |
| -------- | ----------------- | ---------------- |
| 0        | poweroff.target   | Shutdown system  |
| 1        | rescue.target     | Single user mode |

| 2        | multi-user.target | Multi-user mode  |
| 3        | multi-user.target | CLI mode         |
| 4        | multi-user.target | Reserved         |
| 5        | graphical.target  | GUI mode         |
| 6        | reboot.target     | Restart system   |


■ File Types in Linux

■ Types of Files in Linux

Linux has 3 Main File Types

| File Type     | Description                              |
| ------------- | ---------------------------------------- |
| Regular File  | Normal files like text, scripts, configs |
| Directory     | Folder containing files                  |
| Special Files | Hardware & system related files          |


■ Special Files Categories

Special files have 5 categories
| File Type        | Identifier | Description                     |
| ---------------- | ---------- | ------------------------------- |
| Character Device | c          | Keyboard, mouse                 |
| Block Device     | b          | Hard disk, storage              |
| Link             | l          | Soft link / Hard link           |
| Socket File      | s          | Inter-process communication     |
| Named Pipe       | p          | Communication between processes |

■ File Type Identifier

You can identify file type using:

ls -l

Example:
drwxr-xr-x
Here:

First letter indicates file type

d → Directory
rwx → Permissions
root → Owner


| Symbol | File Type        |
| ------ | ---------------- |
| d      | Directory        |
| -      | Regular file     |
| c      | Character device |
| b      | Block device     |
| l      | Link             |
| s      | Socket           |
| p      | Pipe             |

■ Commands

| Command | Usage                  | Example              |
| ------- | ---------------------- | -------------------- |
| file    | Identify file type     | file filename        |
| ls -ld  | Show directory details | ls -ld /home/michael |

■ Hard Links vs Soft Links

| Type      | Description                         |
| --------- | ----------------------------------- |
| Hard Link | Same inode, acts like original file |
| Soft Link | Shortcut to original file           |

Create Hard Link
ln file1 file2

Create soft link 
ln -s  file1 file2

■ Filesystem Hierarchy

Linux follows a hierarchical file system structure starting from:

/
This is called Root Directory

All directories exist under root /

■ Important Directories

| Directory | Usage                     |
| --------- | ------------------------- |
| /         | Root directory            |
| /bin      | Essential user commands   |
| /boot     | Boot loader files         |
| /dev      | Device files              |
| /etc      | Configuration files       |
| /home     | User home directories     |
| /lib      | Shared libraries          |
| /media    | External media mount      |
| /mnt      | Temporary mount directory |
| /opt      | Optional software         |
| /tmp      | Temporary files           |
| /usr      | User programs             |
| /var      | Logs and variable data    |

■ Commands

| Command | Usage                                    | Example |
| ------- | ---------------------------------------- | ------- |
| df -hP  | Show disk usage in human readable format | df -hP  |

df Command Explanation

| Option | Meaning                 |
| ------ | ----------------------- |
| -h     | Human readable (GB, MB) |
| -P     | POSIX format            |

DevOps Usage

Used to:

Check disk usage
Monitor storage
Troubleshoot disk full issues

Common DevOps scenario:

Server issue → Check disk
df -h
Very common troubleshooting command.
