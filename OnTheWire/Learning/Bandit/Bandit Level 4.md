Password = 7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME

## Level Goal

The password for the next level is stored in a hidden file in the **inhere** directory.

This time when i enter ls 
i fond a directory

bandit3@bandit:~$ ls
inhere
so i cd inhere
bandit3@bandit:~$ cd inhere

and then i entered 
bandit3@bandit:~/inhere$ ls

i found nothing

so i tried ls -la to find the hidden files

and i found
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Jun 24 14:59 .
drwxr-xr-x 3 root    root    4096 Jun 24 14:59 ..
-rw-r----- 1 bandit4 bandit3   33 Jun 24 14:59 ...Hiding-From-You

so this time i user cat "filename" to print the content
bandit3@bandit:~/inhere$ cat "...Hiding-From-You"
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq

and i found the password

LEVEL DONE