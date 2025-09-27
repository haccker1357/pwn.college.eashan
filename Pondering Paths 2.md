# Second Module in Linux Luminarium

##Pondering Paths
This Module Contains Nine( 9) Challenges.
  4)Position Elsewhere
  5)Position yet Elsewhere
  6)Implicit Relative Paths, from /
  7)Explicit  Relative Paths, from /

## Position Elsewhere
This challenge will require us to execute the /challenge/run program from a specific directory . We need to cd to that directory before running the challenge program .

**Flag**
pwn.college{062yPSfUbRzLGg7X3ckerBeS7mO.QX3QTN0wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)Open the terminal enter ( /challenge/run ) . It will show as Incorrect,Not using the required directory.
''' bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory
'''
3) Then change the directory to /usr/aarch64-linux-gnu/include/gnu using the ( cd ) command.
4)Then rerun the challenge again to get the required challenge flag.
''' bash
hacker@paths~position-elsewhere:~$ cd /usr/aarch64-linux-gnu/include/gnu
hacker@paths~position-elsewhere:/usr/aarch64-linux-gnu/include/gnu$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{062yPSfUbRzLGg7X3ckerBeS7mO.QX3QTN0wCNyUzNzEzW}
hacker@paths~position-elsewhere:/usr/aarch64-linux-gnu/include/gnu$
'''
5)Success, Now copy and paste the flag in the pwn.college website. And the challenge is completed.

## What I Learned
1)How to launch a terminal and open the programs using absolute path .
 2) All file systems starts from the root directory ( / ) from all other directories, configuration files, programs and folders branch off from which other directories, 
    configuration files, programs and folders branch .
 3)Programs are executed by a definte path called absolute path which starts with the root directory.
 4)Changing the directory.

## Position yet Elsewhere
This challenge will require us to execute the /challenge/run program from a specific directory . We need to cd to that directory before running the challenge program .

**Flag**
pwn.college{0wgbaJcwLZ6fIgKiNjM_zt_ydfH.QX4QTN0wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)Open the terminal enter ( /challenge/run ) . It will show as Incorrect,Not using the required directory.
''' bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /home directory
'''
3) Then change the directory to /home using the ( cd ) command.
4)Then rerun the challenge again to get the required challenge flag.
''' bash
hacker@paths~position-elsewhere:~$ cd /home
hacker@paths~position-elsewhere:/home$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{0wgbaJcwLZ6fIgKiNjM_zt_ydfH.QX4QTN0wCNyUzNzEzW}
hacker@paths~position-elsewhere:/home$
'''
5)Success, Now copy and paste the flag in the pwn.college website. And the challenge is completed.

## What I Learned
1)How to launch a terminal and open the programs using absolute path .
 2) All file systems starts from the root directory ( / ) from all other directories, configuration files, programs and folders branch off from which other directories, 
    configuration files, programs and folders branch .
 3)Programs are executed by a definte path called absolute path which starts with the root directory.
 4)Changing the directory.

"Position thy self":  Positioning to the current directory .
"Position elsewhere": Moving to a different directory than the current one ,using relative or absolute paths.
"Position yet elsewhere": Moving to a different directory than the current one ,using relative or absolute paths.

## Implicit Relative Paths, from /
For this challenge we need to run /challenge/run using a relative path while having a current working directory of /.

**Flag**
pwn.college{g5BkMPJek0A_8X6a78fTHYVz2Va.QX5QTN0wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)We Need to change the directory to ( / ) using the ( cd ) command.
3)Then run the program challenge/run to secure the flag.
''' bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{g5BkMPJek0A_8X6a78fTHYVz2Va.QX5QTN0wCNyUzNzEzW}
hacker@paths~implicit-relative-paths-from-:/$
4) Copy and Paste the flag in the pwn.college website to complete the challenge.

## What i Learned
1)What is Relative path.
Relative Path : Relative path specifies the location of a file or directory relative to the current working directory.
2) Difference between Absolute Path and Relative Path.
Absolute path starts with the root directory while the relative path does't.
But the current working directory ( cwd ) matters in the relative path .

## Explicit  Relative Paths, from /
This challenge need us to use ( . ) Current Directory in the relative paths.

**Flag**
pwn.college{8NpelOHd8jyraxRxDCdbZDxkzfl.QXwUTN0wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)We Need to change the directory to ( / ) using the ( cd ) command.
3)This challenge need us to use the current directory ( . ) in the relative path from the above challenge.
4) We need to run the path ( ./challenge/run ) in the terminal to secure the require flag to complete the challenge.
''' bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path , invoked from the right directory!
Here is your flag:
pwn.college{8NpelOHd8jyraxRxDCdbZDxkzfl.QXwUTN0wCNyUzNzEzW}
'''
5)Copy and Paste the flag in the pwn.college website to complete the challenge.

## What i Learned
1) Learned about explicit relative paths .
2)In most operating systems, including Linux, every directory has two implicit entries that you can reference in paths: ( . ) and ( .. ) .
3) Usage of the first type of explicit path ( Current Directory ) ( . ) .
 challenge
./challenge
./././challenge give the same output
''' bash
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
'''
## Referenceces
I listened and learnt from the videos that are given in the pwn.college website by Hacker Yan.
The Video is ( https://www.youtube.com/watch?v=b67Jq6IZ3U8 )


