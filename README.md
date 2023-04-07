1 What is Linux?

Linux is an open source OS. OS is the software that directly manages a system's hardware and resources, like CPU, memory, and storage.

2 What are the various styles (distributions) of Linux?
```
Debian 
Fedora 
Ubuntu
```

3 What command(s) can you run to identify the style of Linux?

uname -a

4 What is the Linux kernel? 

The Linux kernel is the main component of Linux OS and it handles the OS's primary function. It helps with communication between the user and hardware.

5 How does the kernel differ from an OS?
 
An operating system is a system software that acts as the interface between the users and the machine, while a kernel is a part of the OS that converts user commands into machine language. 


6 What command(s) can you run to locate information on the kernel?


uname -r or -a -a #shows the version of the linux kernel


7 What is a kernel module?

Kernel modules are pieces of code that can be loaded and unloaded into the kernel upon demand. They extend the functionality of the kernel without the need to reboot the system. 

8 How do you list all the kernel modules?

lsmode

9 What is a run-level in Linux?

A run level is a state of init and the whole system that defeines what system services are operating. They are identified by numbers. 

10 How many run-levels are there in Linux?

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

11 How do you change to a different run-level?

Using the init command. 

12 Explain the steps a Linux system goes through when it boots. 

1. BIOS- Baisc Input/Output system. Loads and executes the Master Boot Record boot loader
2. MBR - Master Boot Record, loads and execues the GRUB boot loader. 
3. GRUB - Also GNU GRUB, GNU GRand Unified Bootloader, is the typical boot loader for modern Linux systems. 
4. Kernel- The core of any OS, Linux included. It has complete control over everything in your system. 
5. Init- At this point the system executes runlevel programs. The system looks for an init file, usually found at /etc/inittab to decide the Linux run level. 
6. Runlevel programs- Depending on the Linux distribution installed, you may see different services getting started. These are known as runlevel programs, and are executed from different directories depending on your run level. 

13 What is swap space, why is it important, and what is a typical size for it?

14 What is a symbolic link in Linux? How is it different than a hard link?

15 What is a filesystem? 

16 What are the four fundamental components of every filesystem in Linux? Define each.

17 What is an inode in Linux?

18 Explain what happens to the inode when you run the rm command in Linux.

19 What are the default file descriptors each file gets in Linux and their IDs?

20 What is the name and ID of the first process started by the kernel when Linux starts?

21 Explain the different states a process can be in Linux?

22 How would you find the status of a process in Linux?

23 Describe and explain the different process signals in Linux.

24 How do you debug a running process or a library that is being called in Linux?

25 What is the difference between a SIGKILL and SIGTERM in Linux?



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
