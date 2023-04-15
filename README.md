1 What is Linux?

Linux is an open source OS. OS is the software that directly manages a system's hardware and resources, like CPU, memory, and storage.

2 What is a linux distribution?

Open-source project where all the coders and programmers are combined together andn make some chnages in the Linux kernel by compliling the codes and make it as a new Distro. 



3 What are the various distributions of Linux?
```
Ubuntu
Debian
Fedora
Linux Mint
Cent OS
Manjaro OS
Elementory OS
Zorin OS 
Open Suse
Gentoo
Arch Linux
Kali Linux
Parrot OS
```

4 What command(s) can you run to identify the style of Linux?
```
$ uname -a

Output
Darwin Dutts-MacBook-Pro.local 22.2.0 Darwin Kernel Version 22.2.0: Fri Nov 11 02:08:47 PST 2022; root:xnu-8792.61.2~4/RELEASE_X86_64 x86_64
```
5 What is the Linux kernel? 

The Linux kernel is the main component of Linux OS and it handles the OS's primary function. It helps with communication between the user and hardware.

6 How does the kernel differ from an OS?
 
An operating system is a system software that acts as the interface between the users and the machine, while a kernel is a part of the OS that converts user commands into machine language. 


7 What command(s) can you run to locate information on the kernel?
```
$ uname -r

output
22.2.0
```

8 What is a kernel module?

Kernel modules are pieces of code that can be loaded and unloaded into the kernel upon demand. They extend the functionality of the kernel without the need to reboot the system. 

A purpose for writing a kernel module is to provide a middle layer of code, or common code, thus increasing the efficiency of your system by combining like tasks in a single area and eliminating redundant code.

9 How do you list all the kernel modules?
```
$ lsmod 
for Unix using docker
$ docker run cmd.cat/lsmod lsmod
```
10 What is a run-level in Linux?

A run level is an operating state on a Unix and Unix-based OS that is preset on the Linux-based system. Runlevels determine which programs can execute after the OS boots up and it defines the state of the machine after boot. 


11 How many run-levels are there in Linux?

There are 7 run levels in Linux. 

```
0  System halt i.e the system can be safely powered off with no activity.
1  Single user mode.
2  Multiple user mode with no NFS(network file system).
3  Multiple user mode under the command line interface and not under the graphical user interface.
4  User-definable.
5  Multiple user mode under GUI (graphical user interface) and this is the standard runlevel for most of the LINUX based systems.
6  Reboot which is used to restart the system.
```

12 How do you change to a different run-level?

```
$ init X #X is replaced by the run level you want to change to.  
````

13 Explain the steps a Linux system goes through when it boots. 

1. BIOS - Basic Input/Output system. Loads and executes the Master Boot Record loader.
2. MBR - Master Boot Record, loads and execues the GRUB boot loader. 
3. GRUB - Also GNU GRUB, GNU GRand Unified Bootloader, is the typical boot loader for modern Linux systems. 
4. Kernel - The core of any OS, Linux included. It has complete control over everything in your system. 
5. Init - At this point the system executes runlevel programs. The system looks for an init file, usually found at /etc/inittab to decide the Linux run level. 
6. Runlevel programs - Depending on the Linux distribution installed, you may see different services getting started. These are known as runlevel programs, and are executed from different directories depending on your run level. 

14 What is swap space, why is it important, and what is a typical size for it?

Swap space is used when the amount of physical memory (RAM) is full. If the RAM is full, inactive pages in memory are moved to the swap space. A typical size for swap space is 1 GB or less. 

15 What is a symbolic link in Linux? How is it different than a hard link?

Symbolic links (symlink or soft link) are files that point to a file or directory in your system, but do not mirror the other file's data. Is it like a shortcut in Windoes which contains the path of the original file and its content.

Symbolic link is an actual link to the original file, where a hard link is a mirror copy of the original file. If you delete the original file, the soft link is useless, because it will point to a non-existent file. 

16 What is a filesystem? 

Collection of data and/or files stored in a computer's hard disk or storage, your computer relies on this file system to ascertain the location and positioning of files in your storage. 

17 What are the four fundamental components of every filesystem in Linux? Define each.

```
Superblock - Contains information about the filesystem as a whole, 
such as its size.

Inode - Contains all information about a file, except its name.

Data Block - The inode contains the numbers of several data blocks, which are used to store the data in the file. 

Directory Block - The name is stored in the directory, together with the number of the inode. 

```
Revise last one


18 What is an inode in Linux?

Inode is abbreviation for "index node".

Inode is a data structure that keeps track of all the files and directories within a Linux or UNIX-based filesystem. So every file and directory in a filesystem is allocated an inode, which is identified by an integer known as "inode number". These unique indentifiers store metadata about each file and directory. 

19 Explain what happens to the inode when you run the rm command in Linux.

The system marks the inode belonging to that file as unused and the data blocks of that file also as unused (but not wiped out).

Run it in linux 

20 What are the default file descriptors each file gets in Linux and their IDs?

21 What is the name and ID of the first process started by the kernel when Linux starts?

22 Explain the different states a process can be in Linux?

```
Five Linux process states: 
D = running & runnable (queued up to run or in the process of running).
R = interruptable_sleep (during running, the process will get to a point where it is waiting on data. Ex. User input).
S = uninterruptable_sleep (Process is waiting on something. Ex. mkdir).
T = stopped (Suspended process, command Control+Z, in which the process is put on hold and not responsive).
Z = zombie (Process where the parent has not done this cleanup and you have a process that is lingering. Process has already terminated but it is not quite dead yet.) 
```
23 How would you find the status of a process in Linux?

```
$ ps aux

Output:
  PID TTY           TIME CMD
50429 ttys000    0:03.29 /bin/zsh -il

```
Run in Linux

24 Describe and explain the different process signals in Linux.

```
$ kill-l #lists all the available signals

output
HUP INT QUIT ILL TRAP ABRT EMT FPE KILL BUS SEGV SYS PIPE ALRM TERM URG STOP TSTP CONT CHLD TTIN TTOU IO XCPU XFSZ VTALRM PROF WINCH INFO USR1 USR2
```

```
SIGHUP (1): If a process is running from a terminal and that terminal is closed accidentally, then the process receives this signal. “HUP” is short for “hang up” and terminates the process.

SIGINT (2): Manual interruption of a process from a keyboard. When you hit Ctrl-C, it sends a SIGINT signal to the running process and terminates it.

SIGQUIT(3): When a user types <ctrl>+\ in the terminal. It will force the process to produce a core dump and will terminate the process.

SIGKILL(9): Forcefully terminate a process. This signal can’t be blocked or handled. The receiving process cannot perform clean up when it is terminated with SIGKILL.

SIGPIPE (13): Broken pipe. If a process is piping in its output to another process (producer | consumer) and if the consumer dies, the producer gets the SIGPIPE signal from the consumer, which terminates the producer process

SIGTERM (15): It is the software termination signal. This is the signal that is sent by the kill command by default.

SIGCHLD(17): This signal is sent by a child process to its parent to intimate that the child is stopped or terminated. If a child process terminates before the parent calls the wait syscall on it, the kernel tries to keep the information about the process so that the parent can later call wait to get to know the exit status.

```


26 What is the difference between a SIGKILL and SIGTERM in Linux?

SIGKILL kills the process abruptly, producing a fatal error. Whereas SIGTERM signal can be handled, ignored, and blocked. 


Run it in containers (docker)


To switch directories regardless of your current directory

```
cd
pwd
cd /etc
pwd
Creating a directory inside another directory. Directory 5 is inside directory 4 and directory 6 is inside directory 5. 
mkdir -p dir4/dir5/dir6
-p only if the directory does not exist

```

Command for making a row format into a column format
cat filename

```

Putting the . in front of combined makes the file dissapear (hidden). 
mv combined.txt .combined.txt

```

Command to find out directories vs files
ls -l

```

Command to list the contents of the home directory 
ls ~
Command to count the lines in a file
wc -l filename

Command for creating an emphy file 
touch name of file

Command for removing a file 
rm filename

Command for creating a directory 
mkdir

Command for removing an empty directory
rmdir 

Command for creating a file with text file 
echo "what you want to print" > filename

Command for showing hidden files 
ls -a 

Command for removing non empty directory
rm -R or r name of directory


Creating a directory within a directory 
mkdir hello/hello2

Command to update existing file 
ls > name of file 

Command to add the text into the file  
echo > filename

Redirect stdin and stderr to a file.
ls 2> Welcome
Redirect stdout and stderr to a file.
ls 2>&1 > Welcome  
Redirect stdin , stdout, and stderr to a file.
ls 2> Welcome 
Discard the redirection of stdin, stdout, and stderr.
ls 2> /dev/null
stout redirect to file number 1
ls > 1 
stout and sterr redirected to number 1
echo > Welcome 2>&1
