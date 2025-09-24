# Second Module in Linux Luminarium

##Pondering Paths
This Module Contains Nine( 9) Challenges.
8)Implicit Relative Path
9)Home Sweet Home

##Implicit Relative Path
In this challenge, we'll learn how to explicitly use relative paths to launch run program in this scenario.By executing a program in 
the current directory, using ( . ) current directory, like in the previous challenge. 

**Flag**
pwn.college{MEK5l5nDUh6SMx1EMcuYLu3TDVi.QXxUTN0wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)We Need to change the directory to ( /challenge ) using the ( cd ) command.
3)This challenge need us to use the current directory ( . ) in the relative path to execute.
4) We need to run the path ( ./run ) in the terminal to secure the require flag to complete the challenge.
'''
Connected!
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ run
bash: run: command not found
hacker@paths~implicit-relative-path:/challenge$ ./challenge/run
bash: ./challenge/run: No such file or directory
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{MEK5l5nDUh6SMx1EMcuYLu3TDVi.QXxUTN0wCNyUzNzEzW}
hacker@paths~implicit-relative-path:/challenge$
'''
5)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) Learned about explicit relative paths .
2)In most operating systems, including Linux, every directory has two implicit entries that you can reference in paths: ( . ) and ( .. ) .
3) Usage of the first type of explicit path ( Current Directory ) ( . ) .

##Home Sweet Home
In this challenge, /challenge/run will write a copy of the flag to any file you specify as an argument on the commandline, with some constraints .
 **Flag**
pwn.college{AVWwv3Juy5rsQ3vkzkb6n1-5Ppg.QXzMDO0wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)We need to provide an argument to the command ( /challenge/run ) with some constraints as follows
 1)Your argument must be an absolute path.
 2)The path must be inside your home directory.
 3)Before expansion, your argument must be three characters or less.
3)We need to provide home directory ( ~ ) to the the argument and it must be i an absolute path.
4)So we need to give the argument ( ~/h ) which is just 3 charaters and we need to give space between the command and the argument.
''' bash
Connected!
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{AVWwv3Juy5rsQ3vkzkb6n1-5Ppg.QXzMDO0wCNyUzNzEzW}
hacker@paths~home-sweet-home:~$
'''

#What i Learned
1) ( ~ ) is a directory which is ( /home/hacker ) ,this the expanded version.
2)The home directory is typically where users store most of their personal files. 
3) Generally the home directory will be (/home ) .But in this dojo as we are hacker, our home directory will be ( /home/hacker ).
4)( cd ) will use your home directory as the default destination.
''' bash
hacker@paths~home-sweet-home:~$ cd /
hacker@paths~home-sweet-home:/$ cd
hacker@paths~home-sweet-home:~$
'''

#References
## Referenceces
I listened and learnt from the videos that are given in the pwn.college website by Hacker Yan.
The Video is ( https://www.youtube.com/watch?v=b67Jq6IZ3U8 )




