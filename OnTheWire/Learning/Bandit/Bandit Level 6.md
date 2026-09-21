Password = 6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG


## Level Goal

The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable

this time i connect to the lab and found inhere directory in home
so i moved into it 
this time i found more directory's FUCKING DIRECTORY
so we have a clue that the file is human-readable and its have 1033 bytes in size and not executable
so we use `find` command
we use 
find . -type f -readable -size 1033c ! -executable

bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
maybehere03  maybehere07  maybehere11  maybehere15  maybehere19
bandit5@bandit:~/inhere$ find . -type f -readable -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ find . -type f -readable -size 1033c ! -executable
./maybehere07/.file2
bandit5@bandit:~/inhere$ 

bandit5@bandit:~/inhere$ cd maybehere07
bandit5@bandit:~/inhere/maybehere07$ cat ./-file2
pXa26xhMWaC2SvDotA4r9EgZkulOeSBW

FUCK THE PASSWORD

LEVEL DONE