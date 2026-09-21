Password for Level 1 is = 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
## Level Goal

The password for the next level is stored in a file called **-** located in the home directory

here when we give ls
we got 
`-`
so i tried ls -l
i got 
bandit1@bandit:~$ ls -l
total 4
-rw-r----- 1 bandit2 bandit1 33 Jun 24 14:59 -

So i found that it is a dashed file. so to read the dashed file we need to use cat ./-
`./` - this will help tell the machine that its not a start of the file 

bandit1@bandit:~$ cat ./-
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB

i got password for next LVL

LEVEL DONE


