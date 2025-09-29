##Practicing Piping
This is the sixth module in the Linux Luminarium .
This Module contains 14 challenges
1) Redirecting Output .
2) Redirecting more Output .
3) Appending Output .
4) Redirecting Errors  .

##Redirecting Output
In this challenge, we must use this output redirection to write into the given file.

**Flag**
pwn.college{QuZSE6ZM54mQ7PIXResl3CA4cSI.QX0YTN0wCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) We need to Write the word ( PWN ) to the given file ( COLLEGE )
3) We need to use the output redirection ( > ) to achive this challenge .
4) Enter echo PWN > COLLEGE
5)This will give us the required flag .
``` bash
Connected!
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{QuZSE6ZM54mQ7PIXResl3CA4cSI.QX0YTN0wCNyUzNzEzW}
hacker@piping~redirecting-output:~$
```
6)Copy and Paste the flag in the pwn.college website to complete the challenge.

# Whaat i learned
1) From this challenge we learnt how to redirect standard output to a file.
2) Standard output ( stdout ) redirection ( > ) .
3)Example : hacker@dojo:~$ echo hi > asdf
This will direct the stdout of echo hi to asdf 
hacker@dojo:~$ cat asdf
hi

## Redirecting more Output
This challenge we need to redirect the output of a command to a file .

**Flag**
 pwn.college{grN7Po79Hl3bABsENzVyVTAVv4z.QX1YTN0wCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) Unlike the previous challenge we need to redirect the standard output of a command to the given file .
3) We need to use the output redirection ( > ) to achive this challenge .
4) Enter /challenge/run > myflag
5)After conformation enter cat myflag . To secure the required flag .
``` bash
Connected!
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag
[FLAG] Here is your flag:
[FLAG] pwn.college{grN7Po79Hl3bABsENzVyVTAVv4z.QX1YTN0wCNyUzNzEzW}
hacker@piping~redirecting-more-output:~$
```
6)Copy and Paste the flag in the pwn.college website to complete the challenge.

# Whaat i learned
1) From this challenge we learnt how to redirect standard output to a file.
2) Standard output ( stdout ) redirection ( > ) .
3)Example : hacker@dojo:~$ echo hi > asdf
This will direct the stdout of echo hi to asdf 
hacker@dojo:~$ cat asdf
hi
Just as the avove example we can redirect the stdout of command .

## Appending Output
This challenge run given command with an append-mode redirect of the output to the given file.

**Flag**
pwn.college{cR2pm3jLEFwAGqViuN7eYNovIVi.QX3ATO0wCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) Even we want to store data in the file using stdout redirect . It has a disadvantage ( It will create a new output file every time, deleting the old contents ) .
3)To remove this disadvantage we use append mode using >> instead of > .
4)For this challenge The flag is divided into two parts ,if we want both parts we need to run /challenge/run with an append-mode redirect of the output to the file /home/hacker/the-flag.
5) Enter /challenge/run > /home/hacker/the-flag and after run 9 cat /home/hacker/the-flag ) to get one part of the flag
6) After that we need to run append mode . Enter /challenge/run >> /home/hacker/the-flag this will our required flag in whole .
``` bash
Connected!
hacker@piping~appending-output:~$ /challenge/run > /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag
[HYPE] ONWARDS TO GREATNESS!
[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!
[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...
[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.
[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
m3jLEFwAGqViuN7eYNovIVi.QX3ATO0wCNyUzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag
[HYPE] ONWARDS TO GREATNESS!
[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!
[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...
[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.
[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{cR2pm3jLEFwAGqViuN7eYNovIVi.QX3ATO0wCNyUzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
hacker@piping~appending-output:~$
```
7)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) If we ever wanted to copy a bunch of output in the given file and go over it later we cannot use regular stdout redirect command ( > ),
but we need to use the append mode ( >> ) to check all the outputs later .
2) This challenges teaches us to use the append mode in detail .
3)Example : hacker@dojo:~$ echo pwn > outfile
hacker@dojo:~$ echo college >> outfile
hacker@dojo:~$ cat outfile
pwn
college
hacker@dojo:$

##Redirecting Errors 
Unlike the above challenges , in this challenge we need to redirect the error channel of commands .

**Flag**
pwn.college{EBH-aftPy-WHptOGDBQijUZ8K2_.QX3YTN0wCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) In this challenge, you will need to redirect the output of /challenge/run, like before, to myflag, and the "errors"  to instructions.
3) To redirect errors ( stderr ) we need to use ( 2> ) . Using this character the stderr will be redirected to the given file .
4) Enter  /challenge/run > myflag 2> instructions

``` bash 
Connected!
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag
[FLAG] Here is your flag:
[FLAG] pwn.college{EBH-aftPy-WHptOGDBQijUZ8K2_.QX3YTN0wCNyUzNzEzW}

hacker@piping~redirecting-errors:~$ cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag
[HYPE] ONWARDS TO GREATNESS!
[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.
[TEST] You should have redirected my stdout to a file called myflag. Checking...
[PASS] The file at the other end of my stdout looks okay!
[TEST] You should have redirected my stderr to instructions. Checking...
[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$
```
5)Copy and Paste the flag in the pwn.college website to complete the challenge.

# What i Learned 
1) Just as we redirect the stdout ( output ) to another file , we can also redirect stderr ( error ) to the required file .
2) According to FD 0: Standard Input
FD 1: Standard Output
FD 2: Standard Error
we can use ( 2> ) to redirect the stderr to the required file .
3) File Descriptor numbers. A File Descriptor (FD) is a number that describes a communication channel in Linux. 














