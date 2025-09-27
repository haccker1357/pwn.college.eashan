# Second Module in Linux Luminarium

##Pondering Paths
This Module Contains Nine ( 9 ) Challenges.
   1)The Root.
   2)Program and Absolute Paths.
   3)Position thy Self.

## The Root
In this Challenge, we need to invoke the pwn program using its absolute path, for Capturing the Flag!

*Flag*
pwn.college{QS-esN1S0WwFzYNatUaZ5fOPaFt.QX4cTO0wCNyUzNzEzW}

1) I linked my ubuntu terminal to the pwn.college dojo using public ssh which I generated using `cat key.pub`.

2) Then I connected the required challenge ( The Root ) using ssh command 
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
Now it is Connected to the terminal  

4) Open the terminal and after reading and understanding the challenge, type `/pwn` (directory ) and click enter. We will get the flag that is needed and for completing 
the challenge we need to submit the flag in the given location and then a pop up opens with text Solved `The Root`.
``` bash
Connected!
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{QS-esN1S0WwFzYNatUaZ5fOPaFt.QX4cTO0wCNyUzNzEzW
Success!
```

I read the instructions given under the challenge and noticed that we need to invoke the pwn program using its absolute path.
 ( / ) is the root directory from which all other directories, configuration files, programs and folders branch off.
 ( pwn )  is a program under the root directory.
 ( /pwn ) is command that allows us to open the pwn program that is under the root directory.
this is called the absolute path.

## What I Learned 
1)How to launch a terminal and open the programs using absolute path .
2) All file systems starts from the root directory ( / ) from all other directories, configuration files, programs and folders branch off.
3)Programs are executed by a definte path called absolute path which starts with the root directory.

## Program and Absolute Paths
This challenge requires us to execute run program by invoking its absolute path. We need to execute the run file that is in the challenge directory that is, in turn, 
in the ( / ) root directory. If we invoke the challenge correctly, we will get the flag .

*Flag*
pwn.college{80UPLYSgrJuKSv7yorgMkN61Cet.QX1QTN0wCNyUzNzEzW}

1) I linked my ubuntu terminal to the pwn.college dojo using public ssh which I generated using `cat key.pub` .

2) Then I connected the required challenge ( Intro to Arguments) using ssh command 
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
Now it is Connected to the terminal

3) Open the terminal and after understanding the challenge, type `/challenge/run` 
( directory ) and click enter. We will get the flag that is needed and for completing the challenge we need to submit the flag in the given 
location and then a pop up opens with text Solved `Program Absolut paths`
```bash
Connected!
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{80UPLYSgrJuKSv7yorgMkN61Cet.QX1QTN0wCNyUzNzEzW}
```

I read the instructions given under the challenge and came to the conclusion that we need to invoke the run program using its absolute path.
 ( / ) is the root directory from which all other directories, configuration files, programs and folders branch off.
 ( challenge )  is a directory under the root directory.
 ( run ) is a program that is under the ( challenge ) which is under the root directory.
 ( /challenge/run ) is command that allows us to open the run program that is under the root directory.
this is called the absolute path.

## What I Learned 
 1)How to launch a terminal and open the programs using absolute path .
 2) All file systems starts from the root directory ( / ) from all other directories, configuration files, programs and folders branch off from which other directories, 
    configuration files, programs and folders branch .
 3)Programs are executed by a definte path called absolute path which starts with the root directory.
 4)Unlike the first challenge , we need to use two directories.

## Position thy self
This challenge requires us to execute the absolute path ( /challenge/run ) as in the previous challenge but from another directory. If we invoke the program correctly, we will get the flag

*Flag*
pwn.college{80UPLYSgrJuKSv7yorgMkN61Cet.QX1QTN0wCNyUzNzEzW}

1) I linked my ubuntu terminal to the pwn.college dojo using public ssh which I generated using `cat key.pub` .

2) Then I connected the required challenge ( Intro to Arguments) using ssh command 
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
Now it is Connected to the terminal

3) Open the terminal and after understanding the challenge, type `/challenge/run` ( directory ) and click enter.
4) We will get it has INCORRECT and thats what we need to get then it will mention the directory and then we need to execute the same progrom from that directory.
Then We will get the flag that is needed for the completion of the challenge .
5)After getting the directory we need to channge the directory using ( cd ) command . We need to change into /sys directory rather than ( ~ ) directory.
6)After changing the directory we need to the invokw the run program.

```bash
Connected!
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /sys directory.
Please use the cd utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /sys
hacker@paths~position-thy-self:/sys$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{o8gs40N3lR3cqIupT2IdpKYdOWc.QX2QTN0wCNyUzNzEzW}
Success!
```

I read the instructions given under the challenge and came to the conclusion that we need to invoke the run program using its absolute path from /sys directory.
 ( / ) is the root directory from which all other directories, configuration files, programs and folders branch off.
 ( /sys ) is a type of directory .
 ( challenge )  is a directory under the root directory.
 ( run ) is a program that is under the ( challenge ) which is under the root directory.
 ( /challenge/run ) is command that allows us to open the run program that is under the root directory.
this is called the absolute path.

## What I Learned
 1)How to launch a terminal and open the programs using absolute path .
 2) All file systems starts from the root directory ( / ) from all other directories, configuration files, programs and folders branch off from which other directories, 
    configuration files, programs and folders branch .
 3)Programs are executed by a definte path called absolute path which starts with the root directory.
 4)Changing the directory.
