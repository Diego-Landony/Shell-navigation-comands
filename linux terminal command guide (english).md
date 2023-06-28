# Basic Linux commands (English)
This repository contains a list of useful Linux commands and their possible combinations.
# # command list index and a brief summary:
| Command | Description | 
|---------|-------------|
| [man](#man) | Show the manual of a command |
| [cd](#cd) | Changes the current directory to the one given as the 
argument | | [ls](#ls) | List files and directories |
| [pwd](#pwd) | Displays the current directory the user is in | | [less]
(#less) | Display the content of a text file in the terminal |
| [cat](#cat) | Display the content of one or more text files in the terminal | | 
[file](#file) | Determines the type of a file by examining its contents |
| [ln](#ln) | Create links between files |
| [cp](#cp) | Copy one or more files or directories to another destination 
| | [mv](#mv) | Move or rename one or more files or directories | | [rm]
(#rm) | Delete one or more files or directories |
| [mkdir](#mkdir) | Creates one or more directories with the name given as the argument | | 
[type](#type) | Shows how a command or keyword would be interpreted by the shell | | [which]
(#which) | Shows the full path of executable commands |
| [help](#help) | Displays information about shell built-ins | | [man]
(#man) | Show the manual of a command |
| [find](#find) | Searches for files or directories that meet certain criteria | | 
[chmod](#chmod) | Change access permissions to files or directories | | 
[chown](#chown) | Change the owner and/or group of files or directories | | 
[head](#head) | Display the first few lines of a file or standard input | | [tail]
(#tail) | Show the last few lines of a file or standard input | | [grep](#grep) | 
Search for patterns in files or standard input |
| [ps](#ps) | Shows running processes |
| [top](#top) | Shows the list of running processes in real time | | 
[du](#du) | Shows the space used by files and directories |
| [df](#df) | Shows used and available space on file systems | | [ssh]
(#ssh) | Start a secure remote session on a server |
| [scp](#scp) | Copy files between a local system and a remote system via SSH | | [tar]
(#tar) | Create or extract compressed files in tar format |
| [gzip](#gzip) | Compress or decompress files in gzip format 
| | [unzip](#unzip) | Unzip files in zip format |
| [wget](#wget) | Download files from the web |
| [history](#history) | Shows the history of previously executed commands 
| | [su](#su) | Change to superuser or another user |
| [sudo](#sudo) | Run a command with root privileges |
# # man
The **man** command displays the manual for a command, that is, its description, options, 
arguments, and examples. It is used as follows:
Translated from Spanish to English - www.onlinedoctranslator.com
```bash
man [command]
```
For example, to view the manual for the **ls** command, type:
```bash
man ls
```
##pwd
The **pwd** command displays the current directory the user is in. You don't need any argument. It 
is used like this:
```bash
pwd
```
##ls
The **ls** command lists the files and directories in the current or a specified directory. It can 
be used with different options to modify the format or content of the output. Some common 
options are:
- `-à : show all files, including hidden files (starting with a dot).
- `-l̀ : displays the output in long format, with additional information such as permissions, size, 
owner, and date modified.
- `-h`: Displays the size of files in a human-readable format (for example, KB, MB, GB).
- `-r`: reverses the output order (defaults to ascending alphabetic).
- `-S`: Sorts output by file size, largest to smallest.
- `-t̀ : sorts the output by modification date, from newest to oldest.
It is used in the following way:
```bash
ls [options] [directory] 
```
For example, to list the files in the `/home directory in long format and sorted by size, write:
```bash
ls -lhS /home
```
# # cd
The **cd** command changes the current directory to the one given as the argument. It is used like this:
```bash
cd [directory]
```
For example, to change to the `/usr/bin` directory, type:
```bash
cd /usr/bin
```
If no arguments are specified, the **cd** command changes to the user's home directory (`/
home/[user]`). You can also use the `~` symbol to refer to your home directory.
To return to the previous directory, the `-` argument can be used. For example:
```bash
cd-
```
## less
The **less** command displays the contents of a text file in the terminal, allowing you to 
navigate through it with the arrow keys or the space bar. It is used like this:
```bash
less [file]
```
For example, to view the contents of the `/etc/passwd` file, type:
```bash
less /etc/passwd
```
To exit the **less** command, press the `q` key.
## cat
The **cat** command displays the contents of one or more text files in the terminal, without allowing 
you to scroll through it. It can also be used to concatenate or create files. It is used as follows:
```bash
cat [options] [files] ```
For example, to display the contents of the files `file1.txt̀ and `file2.txt`, write:
```bash
cat file1.txt file2.txt 
```
To create a file called `file3.txt` with the contents of the previous two, the `>̀ operator is used to 
redirect the output. For example:
```bash
cat file1.txt file2.txt > file3.txt ```
## touch
The **touch** command creates an empty file with the name given as the argument. If the file 
already exists, update its modification date. It is used like this:
```bash
touch [file]
```
For example, to create a file called `test.txt̀ , you would type:
```bash
touch test.txt
```
##cp
The **cp** command copies one or more files or directories to another destination. It can be used with 
different options to modify the behavior of the command. Some common options are:
- `-ì : ask before overwriting an existing file.
- `-r`: recursively copies directories and their contents.
- `-v`: show the progress of the copy.
It is used in the following way:
```bash
cp [options] [source] [destination] ```
For example, to copy the file `test.txt̀ to the `/home directory, type:
```bash
cp test.txt /home
```
To copy the `docs` directory and all its contents to the `/homè directory, use the `-r` option. For 
example:
```bash
cp -r docs /home 
```
# #mv
The **mv** command moves or renames one or more files or directories. It can be used with the same 
options as the **cp** command. It is used like this:
```bash
mv [options] [source] [destination] ```
For example, to rename the file `test.txt̀ to `test2.txt`, type:
```bash
mv test.txt test2.txt
```
To move the `test2.txt̀ file to the `/home directory, type:
```bash
mvtest2.txt /home
```
##rm
The **rm** command removes one or more files or directories. It can be used with the same options as 
the **cp** command, plus the following:
- `-f`: force deletion without prompting.
- `-d`: removes an empty directory.
It is used as follows:
```bash
rm [options] [files or directories] 
```
For example, to delete the file `test2.txt̀ , type:
```bash
rm test2.txt
```
To remove the `docs` directory and all its contents, use the `-r` option. For example:
```bash
rm -r docs
```
# # mkdir
The **mkdir** command creates one or more directories with the name given as an argument. It can 
be used with the following options:
- `-p`: create the necessary intermediate directories if they do not exist.
- `-v`: shows the progress of the build.
It is used like this:
```bash
mkdir [options] [directories] 
```
For example, to create a directory called `project`, you would type:
```bash
mkdir project
```
To create a directory structure like `project/src/main`, the `-p` option is used. For example:
```bash
mkdir -p project/src/main 
```
# # rmdir
The **rmdir** command removes one or more empty directories. It can be used with the same options as the 
**mkdir** command. It is used like this:
```bash
rmdir [options] [directories] 
```
For example, to remove the `project/src/main` directory, type:
```bash
rmdir project/src/main 
```
# # file
The **file** command determines the type of a file by examining its contents. It can be used with the 
following options:
- `-b`: Don't print the filename when printing the font.
- `-ì : show the MIME type of the file instead of the human type.
- `-z̀ : tries to examine the contents of the compressed files.
It is used like this:
```bash
file [options] [files] ```
For example, to find out the type of a file called `readme.md`, type:
```bash
file readme.md
```
To display the MIME type of a file named `image.jpg`, the `-ì option is used. For example:
```bash
file -i image.jpg
```
## type
The **type** command shows how a command or keyword would be interpreted by the shell. It can be used 
with the following options:
- `-à : show all locations that contain an executable with the given name.
- `-p`: show the path of the executable if the name is a command.
- `-t̀ : displays a word indicating the type of command: alias, keyword, function, builtin, or file.
It is used like this:
```bash
type [options] [name] 
```
For example, to see how the `ls̀ command is interpreted, type:
```bash
type ls
```
To display all locations that contain an executable named `python`, the `-à option is used. For 
example:
```bash
type -a python
```
# # which
The **which** command displays the full path of executable commands. It can be used with the 
following options:
- `-à : show all matches instead of just the first one.
- `-s̀ : does not print anything, just returns an exit code indicating whether the command exists or not.
It is used like this:
```bash
which [options] [commands] ```
For example, to find out where the `git` command is, you type:
```bash
which git
```
To display all matches of the `python` command, the `-à option is used. For example:
```bash
which -a python
```
# # help
The **help** command displays information about the shell's built-in commands. It can be used with the 
following options:
- `-d`: displays a brief description of each command.
- `-m̀ : displays the information in manual format.
It is used like this:
```bash
help [options] [command] 
```
For example, to view information about the `cd` command, type:
```bash
help cd
```
To view manual format information about the `echo` command, use the `-m̀ option. For 
example:
```bash
help -m echo
```
# # find
The **find** command searches for files or directories that meet certain criteria. It can be used with the 
following options:
- `-name`: search by the name of the file or directory.
- `-typè : search by the type of file or directory (f for files, d for directories, l for symbolic 
links, etc.).
- `-sizè : search by the size of the file or directory.
- `-exec`: Execute a command on the found files or directories.
It is used like this:
```bash
find [options] [path] [expression] 
```
For example, to find all files with the extension `.txt̀ in the current directory, type:
```bash
find . -name "*.txt" 
```
To find all empty directories in the `/home` directory, use the `-type` option and the `-empty` 
expression. For example:
```bash
find /home -type d -empty 
```
To find all files larger than 1 MB and change their permissions to read-only, use the `-sizè option and 
the `-exec̀ option with the `chmod` command. For example:
```bash
find . -size +1M -exec chmod 444 {} \; 
```
# # chmod
The **chmod** command changes the access permissions to files or directories. It can be used with the 
following options:
- `-R`: Applies the permissions change recursively to all files and directories within the 
specified directory.
- `-v`: show the progress of the permissions change.
It is used like this:
```bash
chmod [options] [mode] [file or directory] ```
The mode can be numeric or symbolic. Numeric mode is based on a combination of three digits 
representing read (r), write (w), and execute (x) permissions for owner (u), group (g), and other 
users (o). For example, 644 means that the owner has read and write permission, the group has 
read permission, and all other users have read permission. Symbolic mode relies on the 
symbols +, - and = to add, remove or assign permissions to each category of users. For example, 
u+x means that the execute permission is added to the owner.
For example, to change the permissions of a file called `script.sh` to read-only for all users, 
you can use numeric mode or symbolic mode. For example:
```bash
chmod 444 script.sh
```
either
```bash
chmod a=r script.sh
```
To change the permissions of all files and directories within the `project` directory to read and 
write for the owner and read for the group and other users, use the `-R` option. For example:
```bash
chmod -R 644 project 
```
## chown
The **chown** command changes the owner and/or group of files or directories. It can be used 
with the following options:
- `-R`: applies the owner and/or group change recursively to all files and directories within 
the specified directory.
- `-v`: shows the progress of the owner and/or group change.
It is used like this:
```bash
chown [options] [user]:[group] [file or directory]
```
For example, to change the owner and group of a file named `report.pdf` to 
`john:sales̀ , type:
```bash
chown juan:sales report.pdf 
```
To change only the owner, the group is omitted. For example:
```bash
chown john report.pdf
```
To change just the group, the user is omitted. For example:
```bash
chown :sales report.pdf 
```
To change the owner and group of all files and directories within the `project` directory to 
`ana:development`, the `-R` option is used. For example:
```bash
chown -R ana:develop project ```
## head
The **head** command displays the first few lines of a file or standard input. It can be used with the 
following options:
- `-n`: specifies the number of lines to display. By default they are 10.
- `-c̀ : specifies the number of bytes to display.
- `-q`: Do not display file names.
- `-v`: show the names of the files.
It is used like this:
```bash
head [options] [files] ```
For example, to display the first 5 lines of the `readme.md` file, type:
```bash
head -n 5 readme.md 
```
To display the first 20 bytes of the `readme.md` file, type:
```bash
head -c 20 readme.md 
```
## tail
The **tail** command displays the last few lines of a file or standard input. It can be used 
with the same options as the `head` command, plus:
- `-f`: keep displaying new lines that are added to the end of the file.
- `+n`: shows the lines starting from the nth line.
It is used like this:
```bash
tail [options] [files] ```
For example, to display the last 10 lines of the `readme.md` file, type:
```bash
tail readme.md
```
To display lines 15 to the end of the `readme.md` file, type:
```bash
tail +15 readme.md
```
# # grep
The **grep** command looks for a string in one or more files and displays the lines that contain 
it. It can be used with the following options:
- `-ì : Ignores case differences.
- `-n`: displays the line number of each match.
- `-v`: show lines that do not contain the search string.
- `-r`: Recursively searches all files in a directory and its subdirectories.
It is used like this:
```bash
grep [options] [string] [file(s)] ```
For example, to search for the word `hello in the file `greeting.txt`, type:
```bash
grep hello greeting.txt
```
To search for the word `hello in all files in the current directory, use the `-r` option. For 
example:
```bash
grep -r hello .
```
# # 
The **ps** command displays information about processes running on the system. It can be 
used with the following options:
- `-à : show all processes of all users.
- `-u`: displays the name of the user who started the process and the CPU and memory usage.
- `-x`: show processes that are not associated with a terminal.
- `-è : show all system processes, including kernel processes.
It is used like this:
```bash
ps [options]
```
For example, to view the current user's processes, type:
```bash
ps -u
```
To view all system processes with detailed information, use the `-e` option. For example:
```bash
ps-e
```
## top
The **top** command displays real-time information about processes running on the 
system, sorted by CPU or memory usage. It can be used with the following options:
- `-d`: Specifies the time interval between each update, in seconds.
- `-p`: shows only the processes with the identifiers (PID) indicated.
- `-u`: show only the processes of the indicated user.
- `-o`: Sort processes by the specified field, such as `CPU`, `MEM`, `TIMÈ , etc.
It is used like this:
```bash
top [options]
```
For example, to see which processes are consuming the most CPU, type:
```bash
top -o cpu
```
To see only the processes of the `root̀ user, use the `-u` option. For example:
```bash
top -u root
```
# #du
The **du** command displays the space occupied by one or more files or directories. It can be used 
with the following options:
- `-h` : Displays the size in human-readable units, such as `K`, `M`, `G̀ , etc.
- `-s̀ : show only the total size of each argument, without breaking down by subdirectories.
- `-à : show the size of all files, not just directories.
- `-c̀ : displays the total size of all arguments.
It is used like this:
```bash
du [options] [file(s) or directory(s)] ```
For example, to see the space occupied by the `project` directory, type:
```bash
your project
```
To see the space occupied by the `project` directory and its subdirectories, use the `-h` option. For 
example:
```bash
du -h project
```
##df
The **df** command displays the space available and occupied by the disk partitions. It can be used 
with the following options:
- `-h` : Displays the size in human-readable units, such as `K`, `M`, `G̀ , etc.
- `-T̀ : shows the file system type of each partition.
- `-à : show all partitions, including those without a mount point.
- `-ì : shows the number of inodes available and used by each partition.
It is used like this:
```bash
df [options]
```
For example, to see the space available and occupied by the disk partitions, type:
```bash
df
```
To see the type of file system and the number of inodes for each partition, use the `- T̀ and `-ì 
options. For example:
```bash
df-Ti
```
# # ssh
The **ssh** command allows you to establish a secure connection to a remote server using 
the Secure Shell protocol. It can be used to access a GitHub repository or to run commands 
on the server. It can be used with the following options:
- `-ì : specifies the file that contains the private key for authentication.
- `-p`: specifies the port to which you want to connect.
- `-v`: displays detailed information about the connection.
It is used like this:
```bash
ssh [options] [user@]host 
```
For example, to connect to the GitHub server using the private key `id_rsa`, type:
```bash
ssh -i rsa_id git@github.com 
```
## scp
The **scp** command allows you to copy files or directories between a remote server and the local 
machine using the Secure Shell protocol. It can be used to upload or download files from a GitHub 
repository. It can be used with the following options:
- `-ì : specifies the file that contains the private key for authentication.
- `-p`: preserves the attributes of the copied files.
- `-r`: recursively copies directories and their contents.
- `-v`: display detailed information about the copy.
It is used like this:
```bash
scp [options] source destination 
```
For example, to copy the `readme.md` file from the local repository to the GitHub server, 
type:
```bash
scp -i rsa_id readme.md git@github.com :user/repository.git ```
To copy the `project` directory from the GitHub server to the local `~/Documents` directory, use the 
`-r` option. For example:
```bash
scp -r -i rsa_id git@github.com :user/project.git ~/Documents ```
# # tar
The **tar** command allows you to create or extract compressed files in tar format. It can be used 
to pack multiple files or directories into one, making it easy to transport or store. It can be used 
with the following options:
- `-c̀ : creates a tar file.
- `-x`: extract a tar file.
- `-f`: Specifies the name of the tar file.
- `-v`: shows the names of the processed files.
- `-z̀ : compress or decompress the tar file using gzip.
It is used like this:
```bash
tar [options] [archive] 
```
For example, to create a tar file named `project.tar.gz̀ containing the `project` directory and its 
subdirectories, use the `-c̀ , `-f` , and `-z̀ options. For example:
```bash
tar -czf project.tar.gz project 
```
To extract the contents of the tar file `project.tar.gz̀ into the current directory, use the `- x`, `-f` and `-z̀ 
options. For example:
```bash
tar -xzf project.tar.gz 
```
## gzip
The **gzip** command allows you to compress or decompress files using the gzip 
compression algorithm. It can be used to reduce file sizes and save disk or network space. It 
can be used with the following options:
- `-d`: decompress the file.
- `-k`: Keep the original uncompressed file.
- `-l̀ : display information about the compressed file.
- `-v`: displays the name and compression ratio of the file.
It is used like this:
```bash
gzip [options] [file] ```
For example, to compress the file `readme.md` and replace it with `readme.md.gz̀ , write:
```bash
gzip readme.md
```
To decompress the `readme.md.gz` file and keep the original, use the `-k` option. For 
example:
```bash
gzip -dk readme.md.gz
```
# # unzip
The **unzip** command allows you to extract compressed files in zip format. It can be used 
to unzip files downloaded from the Internet or sent by email. It can be used with the following 
options:
- `-d`: Specifies the directory where the files will be extracted.
- `-l̀ : display the contents of the zip file without extracting it.
- `-v`: displays detailed information about the zip file and the extracted files.
It is used like this:
```bash
unzip [options] [file] ```
For example, to extract the contents of the zip file `project.zip` to the current directory, you would type:
```bash
unzip project.zip
```
To extract the contents of the zip file `project.zip` into the `~/Documents̀ directory, use the `-d` 
option. For example:
```bash
unzip -d ~/Documents project.zip ```
##wget
The **wget** command allows you to download files or web pages from the Internet. It can be used to get 
resources from GitHub or other sources. It can be used with the following options:
- `-Ò : specifies the name of the output file.
- `-P`: specifies the directory where the downloaded file will be saved.
- `-q`: Do not display messages or progress indicators.
- `-v`: displays detailed information about the download.
It is used like this:
```bash
wget [options] [url]
```
For example, to download the file `readme.md` from the GitHub repository `user/project.git̀ 
and save it as `project_readme.md` in the current directory, use the `-O` and `-q` options. 
For example:
```bash
wget -O project_readme.md -q https://raw.githubusercontent.com/user/
project.git/master/readme.md ```
## history
The **history** command allows you to display or manipulate the history of commands executed in the 
terminal. It can be used to review or repeat previous commands. It can be used with the following options:
- `-c̀ : clears the command history.
- `-d`: removes a history entry by specifying its number.
- `-r`: read the command history from a file.
- `-ẁ : write the command history to a file.
It is used like this:
```bash
history [options] [number] 
```
For example, to display the last 10 commands executed, type:
```bash
history 10
```
To repeat command number 5 from the history, the exclamation mark is used. For example:
```bash
!5
```
# # his
The **su** command allows you to switch users in the terminal. It can be used to run commands with 
another user's privileges. It can be used with the following options:
- `-`: Start a login session for the new user.
- `-c̀ : Run a command as the new user, then revert to the old user.
- `-l̀ : display information about the new user.
It is used like this:
```bash
su [options] [user] ```
For example, to change to the user `root̀ , type:
```bash
su root
```
To run the `ls` command as the `root̀ user and then return to the current user, use the `- c̀ option. For 
example:
```bash
su -c ls root
```
# # sudo
The **sudo** command allows you to run a command as another user, usually superuser or 
administrator. It can be used to perform tasks that require special permissions. It can be used with 
the following options:
- `-u`: specifies the user you want to run the command as.
- `-l̀ : displays the commands that can be executed with sudo.
- `-k`: invalidates the cached password and prompts for a new one.
- `-v`: Checks the cached password and updates it.
It is used like this:
```bash
sudo [options] [command] 
```
For example, to run the `apt update' command as the root user, type:
```bash
sudo apt update
```
To run the `ls` command as user `john`, use the `-u` option. For example:
```bash
sudo -u john ls
```
:)
