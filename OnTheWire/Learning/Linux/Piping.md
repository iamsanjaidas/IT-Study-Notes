So far we've dealt with sending data to and from files. Now we'll take a look at a mechanism for sending data from one program to another. It's called piping and the operator we use is ( | ) (found above the backslash ( \ ) key on most keyboards). What this operator does is feed the output from the program on the left as input to the program on the right. In the example below we will list only the first 3 files in the directory.

![[Pasted image 20260921204713.png]]

We may pipe as many programs together as we like. In the below example we have then piped the output to tail so as to get only the third file.

![[Pasted image 20260921204740.png]]

```
TIP :
- Any command line arguments we supply for a program must be next to that program.
- I often find people try and write their pipes all out in one go and make a mistake somewhere along the line. They then think it is in one point but in fact it is another point. They waste a lot of time trying to fix a problem that is not there while not seeing the problem that is there. If you build your pipes up incrementally then you won't fall into this trap. Run the first program and make sure it provides the output you were expecting. Then add the second program and check again before adding the third and so on. This will save you a lot of frustration.
```

You may combine pipes and redirection too.
![[Pasted image 20260921204850.png]]