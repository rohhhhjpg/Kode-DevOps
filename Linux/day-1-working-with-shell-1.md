# ■ Working With Shell — Part 1

## ■ Commands Learned

| Command | Usage                                   | Example        |
| ------- | --------------------------------------- | -------------- |
| echo    | Print the output on screen              | echo rohit     |
| echo -n | Print the output without new trail line | echo -n rohit  |

## ■ Basic Linux Commands 

| Command  | Usage                                            | Example               |
| -------- | ------------------------------------------------ | --------------------- |
| pwd      | Present working directory                        | pwd                   |
| ls       | List files and directories                       | ls                    |
| mkdir    | Create directory                                 | mkdir test            |
| cd       | Change directory                                 | cd test               |
| mkdir -p | Create parent and child directory                | mkdir -p India/Mumbai |
| pushd    | Save current directory and move to new directory | pushd /home           |
| popd     | Return to previous directory                     | popd                  |
| mv       | Move or rename files/directories                 | mv file1 file2        |
| cp       | Copy files                                       | cp file1 file2        |
| rm       | Remove file                                      | rm file.txt           |
| cp -r    | Copy directory recursively                       | cp -r folder1 folder2 |
| cat      | Display file contents                            | cat file.txt          |
| cat >    | Create file and write content                    | cat > file.txt        |
| touch    | Create empty file                                | touch file.txt        |
| more     | View file page by page                           | more file.txt         |
| less     | View file with scroll support                    | less file.txt         |
| ls -l    | Long listing format                              | ls -l                 |
| ls -a    | Show hidden files                                | ls -a                 |
| ls -lt   | Sort by modified time                            | ls -lt                |
| ls -ltr  | Sort by time in reverse                          | ls -ltr               |

■ more Command Shortcuts

| Key   | Action          |
| ----- | --------------- |
| Space | Scroll forward  |
| Enter | Scroll one line |
| b     | Scroll backward |
| /     | Search text     |

■ less Command Shortcuts

| Key        | Action      |
| ---------- | ----------- |
| Up Arrow   | Scroll up   |
| Down Arrow | Scroll down |
| /          | Search text |

■ Command-line Help Commands

| Command | Usage                                      | Example          |
| ------- | ------------------------------------------ | ---------------- |
| whatis  | Shows short description of a command       | whatis date      |
| man     | Displays detailed manual page of a command | man date         |
| --help  | Shows command help and options             | date --help      |
| apropos | Search commands related to a keyword       | apropos modprobe |

■ Bash Environment & Prompt Commands

| Command     | Usage                       | Example                        |
| ----------- | --------------------------- | ------------------------------ |
| echo $SHELL | Displays current shell      | echo $SHELL                    |
| chsh        | Change default shell        | chsh -s /bin/bash              |
| alias       | Create shortcut for command | alias dt=date                  |
| env         | Show environment variables  | env                            |
| export      | Create environment variable | export OFFICE=caleston         |
| echo $PATH  | Show executable paths       | echo $PATH                     |
| which       | Show command location       | which python                   |
| export PATH | Add new command path        | export PATH=$PATH:/opt/obs/bin |
| echo $PS1   | Show bash prompt format     | echo $PS1                      |
| PS1="text"  | Change prompt format        | PS1="ubuntu-server:"           |

■ Bash Prompt Variables

| Variable | Usage                  |
| -------- | ---------------------- |
| \d       | Date                   |
| \h       | Hostname               |
| \H       | Full hostname          |
| \n       | New line               |
| \r       | Carriage return        |
| \s       | Shell name             |
| \t       | Time (24 hour)         |
| \T       | Time (12 hour)         |
| @        | Time am/pm             |
| \A       | Time (HH:MM)           |
| \u       | Username               |
| \w       | Current directory      |
| \W       | Directory basename     |
| $        | # for root, $ for user |

■ Bash Prompt Example

Input: PS1="[\d \t \u@\h: \w ] $ "
Output: Tue Apr 08 14:22 user@server: /home $


■ Environment Variables Permanent Save
Temporary:
export OFFICE=caleston

Permanent:

Store in:
~/.profile
~/.pam_environment



---

## ■ Notes

* Commands can work with argumanets and some inbuilt commands can run without arguments too.
* Internal or Built in commands - echo , cd , pwd , set e.t.c
* External commands - mv, date, uptime, cp, uptime e.t.c
* Use type command to find whether the command is internal or external
* ~ - Represents home directory in linux
* Different types of shell , Bourne Shell (sh) , C shell, Korn shell, Z shell, Bourne again shell (Bash)
