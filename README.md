To switch directories regardless of your current directory
cd
pwd
cd /etc
pwd
Creating a directory inside another directory. Directory 5 is inside directory 4 and directory 6 is inside directory 5. 
mkdir -p dir4/dir5/dir6
-p only if the directory does not exist

Command for making a row format into a column format
cat filename

Putting the . in front of combined makes the file dissapear (hidden). 
mv combined.txt .combined.txt

Command to find out directories vs files
ls -l

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