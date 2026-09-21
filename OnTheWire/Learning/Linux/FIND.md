Here we learn about find command 
it is the most use full command because it very powerful.
it is used to find a something in the whole Linux tree


TO user this command we need to 

find <what i need to find?>
example if i need to find a .log file in a linux tree i can use

find / -type f -name "*.log"

if i need to find a .log file in current directory i can use

find . -type f -name ".log"

lets elobrate

/ is the root so it will search form / 
. is the current directory so it will search from there
 we used -type 
 so `f` here is file we can also use `d` for directory
 also we can input -readable to find a file which is only readable by the current user 
 if we add ! in front it will consider this as non-readable file 
 find . -type f -readable
 find . -type f ! -readable

next 

-name which is used for searching name of the file or directory and its case-sensitive
-iname which is also used to search name of the file or directory but its not case-sensitive
why we user  `*.log` becasue `*` is used for all in linux so example we dont know the file name but we know its a log file we can use this `*.log`

-size
which is used to help find the file which we know the file size
example : we want to find a file which are more than 20gb of log file in /var/log/
so we use:
`find /var/log -type f -name "*.log" -size +20g`

in size we can set 3 type
`+number` will find size which is greater than then the number
`-number` will find size which is lesser than then the number
`number` will find size which is exactly equals to the number

and there are units
c = bytes
k = KiB (1024 bytes)
m = MiB
g = GiB
T = TiB
w = 2-byte words
No suffix = 512-byte blocks

Now we go deep 

find the file with particular permissions 
-readable
-writable
-executable
and there are operators
FUCKING BIG 3
-o --> OR
! --> NOT
condition1 condition 2 --> AND

so if we are going to use 2 diffrent operatiors we need to use parentheses :

`\(     \)`
so lets try a example
we are going to find a file in current directory which need to have either read permission or executable permission so we use
`find -type f \(-readable -o -executable \)`

another example 
we are going to find a file in current directory which dont have either read permission or executable permission so we use
`find -type f \(! -readable -o ! -executable \)`

-perm
now lets learn how to use -perm :
which is used to search using exact permission
example 
`find . -type f -perm 644`
which will find the file in current directory which have owner - read and write permission while group have read only
and other have read only permission

so -perm 644 means
`-rw-r--r--`

find by who owned the file 
-user
-group
-other

example :
a file is owned by user sanjai and owner by group IT_support
we can use
`find / -type f -user sanjai -group IT_support`

but here we get so many fucking denied permission errors so we remove those error by using
2>/dev/null
why ? and how ?
`2>` redirect file descrptors 
2 - stderr (error messages)
/dev/null - its a black hole
/dev/null is a trash anything we put there will discareed dimmeditely
if we need to have those errors message we can use 2> error.txt 
`0 --> stdin --> input
`1 --> stdout --> normal output`
`2--> stderr --> errors`

SO FIND IS VERY USEFUL

BEST WAY TO REMEMBER IS TO UNDERSTAND FIND AS

`FIND <WHERE> <WHAT TO SEARCH FOR> <WHAT TO DO>`

