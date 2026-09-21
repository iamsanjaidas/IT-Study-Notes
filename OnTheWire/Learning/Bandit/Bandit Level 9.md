
Password = VR1ljMayciFxbnUokuQmJFw6QC9VKtub

## Level Goal

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once


so this level we learn sort and piping
so when i use `ls`
i found a data.txt file

that contact tons of shit

so i need to sort that and help find the password
fuck that after using sort data.txt
i found so many fake password and they are repeating so my guess is that i need to find one which is not repeating 

so i need to use `uniq -u` which will display the unique line in data.txt
which i need to get the input from sort data.txt output
so i will do the piping here

`sort data.txt | uniq -u`
using this i found the key 
bandit8@bandit:~$ sort data.txt | uniq -u
EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl

LEVEL DONE

