■ Package Management

Linux uses Package Managers to:

Install software
Remove software
Update packages
Manage dependencies

■ Package Types

| Package Type | Distribution               |
| ------------ | -------------------------- |
| .RPM         | RHEL, CentOS, Fedora       |
| .DEB         | Ubuntu, Debian, Linux Mint |

■ Package Managers

| Package Manager | Distribution |
| --------------- | ------------ |
| DPKG            | Debian based |
| APT             | Debian based |
| APT-GET         | Debian based |
| RPM             | RPM based    |
| YUM             | RPM based    |
| DNF             | RPM based    |

■ Functions of Package Managers
Package Integrity
Package Authenticity
Simplified Package Management
Grouping Packages
Manage Dependencies

■ DPKG Commands

| Command | Usage           | Example          |
| ------- | --------------- | ---------------- |
| dpkg -i | Install package | dpkg -i gimp.deb |

Error occurs when dependencies missing


■ RPM Commands (5 Basic Modes)

| Command  | Usage           | Example                 |
| -------- | --------------- | ----------------------- |
| rpm -ivh | Install package | rpm -ivh telnet.rpm     |
| rpm -e   | Remove package  | rpm -e telnet.rpm       |
| rpm -Uvh | Upgrade package | rpm -Uvh telnet.rpm     |
| rpm -q   | Query package   | rpm -q telnet           |
| rpm -Vf  | Verify package  | rpm -Vf /usr/bin/telnet |

Important Note

RPM does not resolve dependencies automatically

That's why YUM is used.

■ YUM Package Manager

High level package manager for:

RHEL
CentOS
Fedora

Resolves dependencies automatically.

■ YUM Commands

| Command            | Usage                          | Example           |
| ------------------ | ------------------------------ | ----------------- |
| yum install        | Install package                | yum install httpd |
| yum repolist       | List repositories              | yum repolist      |
| yum provides       | Find package providing command | yum provides scp  |
| yum remove         | Remove package                 | yum remove httpd  |
| yum update package | Update specific package        | yum update telnet |
| yum update         | Update all packages            | yum update        |

■ YUM Features
RPM based distros
Software repositories
High level package manager
Automatic dependency resolution



■ DPKG Utility (Debian Package Manager)

Used in:

Ubuntu
Debian
Linux Mint

■ DPKG Commands

| Command | Usage                       | Example            |
| ------- | --------------------------- | ------------------ |
| dpkg -i | Install package             | dpkg -i telnet.deb |
| dpkg -r | Remove package              | dpkg -r telnet     |
| dpkg -l | List installed package      | dpkg -l telnet     |
| dpkg -s | Show package status         | dpkg -s telnet     |
| dpkg -p | Show package info from file | dpkg -p telnet.deb |

■ APT / APT-GET

APT is high level package manager
Resolves dependencies automatically

We mostly use:
APT instead of APT-GET

■ APT Commands

| Command          | Usage                     | Example                |
| ---------------- | ------------------------- | ---------------------- |
| apt install      | Install package           | apt install gimp       |
| apt update       | Update repository list    | apt update             |
| apt upgrade      | Upgrade packages          | apt upgrade            |
| apt edit-sources | Edit repository sources   | apt edit-sources       |
| apt remove       | Remove package            | apt remove telnet      |
| apt search       | Search package            | apt search telnet      |
| apt list | grep  | Filter installed packages | apt list | grep telnet |


■ APT-GET Commands

| Command          | Usage           | Example                 |
| ---------------- | --------------- | ----------------------- |
| apt-get install  | Install package | apt-get install gimp    |
| apt-cache search | Search package  | apt-cache search telnet |


■ APT vs APT-GET

| APT                   | APT-GET             |
| --------------------- | ------------------- |
| User friendly output  | Less user friendly  |
| Recommended for users | Older utility       |
| Simple commands       | More verbose output |

Example
APT Search:
apt search telnet

APT-GET Search:
apt-cache search telnet
APT-GET throws more detailed output.

Important Note:
APT resolves dependencies automatically
Unlike:
dpkg
rpm
Which require manual dependency installation.
