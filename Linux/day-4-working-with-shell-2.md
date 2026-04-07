■ Working With Shell — Part 2

■ File Size Commands

| Command | Usage                                     | Example         |
| ------- | ----------------------------------------- | --------------- |
| du -sh  | Show directory/file size (human readable) | du -sh test.img |
| ls -lh  | Show file size in human readable format   | ls -lh test.img |
| du -sk  | Show file size in KB                      | du -sk test.img |

■ Tar Commands (Archiving)

| Command  | Usage                        | Example                            |
| -------- | ---------------------------- | ---------------------------------- |
| tar -cf  | Create tar archive           | tar -cf test.tar file1 file2 file3 |
| tar -tf  | List tar file contents       | tar -tf test.tar                   |
| tar -xf  | Extract tar file             | tar -xf test.tar                   |
| tar -zcf | Create compressed tar (gzip) | tar -zcf test.tar.gz file1 file2   |

■ Compression Commands
bzip2
| Command | Usage                 | Example             |
| ------- | --------------------- | ------------------- |
| bzip2   | Compress file         | bzip2 test.img      |
| du -sh  | Check compressed size | du -sh test.img.bz2 |

gzip
| Command | Usage                 | Example             |
| ------- | --------------------- | ------------------- |
| gzip    | Compress file         | gzip test1.img      |
| du -sh  | Check compressed size | du -sh test1.img.gz |

xz
| Command | Usage                 | Example             |
| ------- | --------------------- | ------------------- |
| xz      | Compress file         | xz test2.img        |
| du -sh  | Check compressed size | du -sh test2.img.xz |

■ Uncompress Commands

bunzip2
| Command | Usage               | Example              |
| ------- | ------------------- | -------------------- |
| bunzip2 | Uncompress bz2 file | bunzip2 test.img.bz2 |
| du -sh  | Check size          | du -sh test.img      |

gunzip
| Command | Usage                | Example             |
| ------- | -------------------- | ------------------- |
| gunzip  | Uncompress gzip file | gunzip test1.img.gz |
| du -sh  | Check size           | du -sh test1.img    |

unxz
| Command | Usage              | Example           |
| ------- | ------------------ | ----------------- |
| unxz    | Uncompress xz file | unxz test2.img.xz |
| du -sh  | Check size         | du -sh test2.img  |

■ View Compressed Files Without Extracting

| Command | Usage          | Example        |
| ------- | -------------- | -------------- |
| zcat    | View gzip file | zcat file.gz   |
| bzcat   | View bzip file | bzcat file.bz2 |
| xzcat   | View xz file   | xzcat file.xz  |


■ Searching Files and Directories

| Command  | Usage                  | Example                           |
| -------- | ---------------------- | --------------------------------- |
| locate   | Find file quickly      | locate city.txt                   |
| updatedb | Update locate database | updatedb                          |
| find     | Search file manually   | find /home/michael -name city.txt |

■ GREP Commands

| Command      | Usage                     | Example                                       |
| ------------ | ------------------------- | --------------------------------------------- |
| grep         | Search text in file       | grep second sample.txt                        |
| grep -i      | Case insensitive search   | grep -i capital sample.txt                    |
| grep -r      | Recursive search          | grep -r "third line" /home/michael            |
| grep -v      | Print non matching lines  | grep -v "printed" sample.txt                  |
| grep -w      | Match whole word          | grep -w exam example.txt                      |
| grep -vw     | Invert whole word match   | grep -vw exam examples.txt                    |
| grep -A1     | Show line after match     | grep -A1 Arsenal premier-league-table.txt     |
| grep -B1     | Show line before match    | grep -B1 4 premier-league-table.txt           |
| grep -A1 -B1 | Show before & after lines | grep -A1 -B1 Chelsea premier-league-table.txt |

■ Input Output Redirection
Three Data Streams

| Stream | Description     |
| ------ | --------------- |
| stdin  | Standard input  |
| stdout | Standard output |
| stderr | Standard error  |

■ Redirect stdout

| Command | Usage                   | Example                          |
| ------- | ----------------------- | -------------------------------- |
| >       | Redirect output to file | echo $SHELL > shell.txt          |
| >>      | Append output           | echo "This is bash" >> shell.txt |


■ Redirect stderr

| Command   | Usage                 | Example                        |
| --------- | --------------------- | ------------------------------ |
| 2>        | Redirect error output | cat missing_file 2> error.txt  |
| 2>>       | Append error output   | cat missing_file 2>> shell.txt |
| /dev/null | Ignore errors         | cat missing_file 2> /dev/null  |

■ Command Line Pipes

Pipe symbol:

|
Used to link multiple commands
Example
grep Hello sample.txt | less

■ Tee Command

| Command | Usage                    | Example                                |
| ------- | ------------------------ | -------------------------------------- |
| tee     | Display and store output | echo $SHELL | tee shell.txt            |
| tee -a  | Append output            | echo "This is bash" | tee -a shell.txt |


