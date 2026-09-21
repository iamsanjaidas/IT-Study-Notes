Password = xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
## Level Goal

The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

this time i found a directory inhere using ls

so i moved to that directory 
and after entering ls
i found 9 files which dashed file FUCK THAT SHIT
so when i opened the file -file00 i found that 
SHIT IS MESSED UP
so this time i tried a different approach find find the human readable file which is ASCII so to do that i used `file` command
and found out that -file07 is that SHIT
so i opened it and found that next level password

bandit4@bandit:~$ ls 
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file02  -file04  -file06  -file08
-file01  -file03  -file05  -file07  -file09
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: OpenPGP Public Key
./-file07: ASCII text
./-file08: data
./-file09: Motorola S-Record; binary data in text format
bandit4@bandit:~/inhere$ cat ./-file07
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG


LEVEL DONE 