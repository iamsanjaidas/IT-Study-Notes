## Level Goal

The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Commands you may need to solve this level
 ls, cat, cd, file, du, find

`ls
bandit0@bandit:~$ ls
readme`

Cat
`bandit0@bandit:~$ cat readme
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: `6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR`
`

bandit0@bandit:~$ file readme
readme: ASCII text

bandit0@bandit:~$ du -h
20K	.

bandit0@bandit:~$ find readme
readme

LEVEL DONE 
Password for Level 1 is = 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
