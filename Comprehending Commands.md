#Comprehending Commands
This  is the third module in the the Linux Luminarium.This Module contains 14 challenges.
1) cat :not the pet , but the command.
2) Catting absolute paths .
3) More Catting Pratice .
4) Grepping for a needle in a hay stack . 
5) Comparing files . 

## cat :not the pet , but the command
In this challenge we need to use the ( cat ) command to the file name ( flag ) to display  the flag.

**Flag**
pwn.college{YuH1hQXwH48CW7PiO-N6y7sdkBG.QXxcTN0wCNyUzNzEzW}

##Process
1)First we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)We need to use the ( cat ) command to display the flag in the ( flag ) file.
3)Enter cat flag to display the file in it.
``` bash
Connected!
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{YuH1hQXwH48CW7PiO-N6y7sdkBG.QXxcTN0wCNyUzNzEzW}
hacker@commands~cat-not-the-pet-but-the-command:~$
```
#What i Learned
1)I learned what a cat command is and the functions of it
  cat is generally used for reading out files.
and concatenate multiple files if provided multiple arguments.
2)How to use the cat command

## Catting absolute paths
In this challenge we need to use the ( cat ) command to the absolute path ( /flag ) to display  the flag.

 **Flag**
pwn.college{UoTrhHAltdjvaGKSMTTUJxfZdp_.QX5ETO0wCNyUzNzEzW}

##Process
1)First we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)We need to use the ( cat ) command to display the flag in the ( flag ) file which is in the home directory using absolute path.
3)Enter cat /flag to display the file in it.
``` bash
Connected!
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{UoTrhHAltdjvaGKSMTTUJxfZdp_.QX5ETO0wCNyUzNzEzW}
hacker@commands~catting-absolute-paths:~$
```
#What i Learned
1)I learned what a cat command is and the functions of it
  cat is generally used for reading out files.
and concatenate multiple files if provided multiple arguments.
2)How to use the cat command
3)We can use cat command for reading files using absolute paths too.

# More Catting Pratice
In this challenge, The flag in some crazy directory, with no changing directories with cd .Then we can retrive the flag.

**Flag**
pwn.college{8Nlee42Hge-DzENWmAz4S0ctKqG.QXwITO0wCNyUzNzEzW}

##Process
1)First we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)We need to use the the directory they mentioned with the cat argument to secure the flag.
3)Enter cat /lib/groff/flag to get the flag that is stored in the file flag.
``` bash
Connected!
You cannot use the `cd` command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /lib/groff/flag. Go cat it out *without* cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /lib/groff/flag
pwn.college{8Nlee42Hge-DzENWmAz4S0ctKqG.QXwITO0wCNyUzNzEzW}
hacker@commands~more-catting-practice:~$
```
#What i learned
1)I learned what a cat command is and the functions of it
  cat is generally used for reading out files.
and concatenate multiple files if provided multiple arguments.
2)How to use the cat command
3)We can use cat command for reading files using absolute paths too.

## Grepping for a needle in a hay stack.
In this challenge we need to find the flag which in a file provided with the command ( grep ).

**Flag**
pwn.college{Mho3N_ppIeKaOSTvELeQ594Ulw6.QX3EDO0wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)We need to use the the code word they mentioned with the grep command and the file location to secure the flag.
3) Structure grep codeword ( file needed to be searched in absolute path )
4)They told us that the flag is situated in a file ( /challenge/data.txt ) and with code word as ( pwn.college ).
5)Enter grep pwn.college /challenge/data.txt in the terminal .
``` bash
Connected!
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{Mho3N_ppIeKaOSTvELeQ594Ulw6.QX3EDO0wCNyUzNzEzW}
hacker@commands~grepping-for-a-needle-in-a-haystack:~$
```
6) Copy and Paste this flag in the pwn.college website to complete the challenge.

#What i Learned
1) I learned how to use grep command and what is it is .
Grep :Grep allows us to quickly search for specific patterns, words, or phrases within one or more text files. 
2) Structure : grep codeword ( file needed to be searched in absolute path )

## Comparing files
This challenge involves us to compare between two files and find the flag which is the difference between the two files.

 **Flag**
pwn.college{QQUMVd7vLifbl1i0yIXWH8QzuBL.01MwMDOxwCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)We need to use the two files they montioned 
 1)/challenge/decoys_only.txt contains 100 fake flags .
 2)/challenge/decoys_and_real.txt contains all 100 fake flags plus the one real flag .
3)Structure diff file1 file 2 
```
hacker@dojo:~$ cat old
pwn
hacker@dojo:~$ cat new
pwn
college
hacker@dojo:~$ diff old new
1a2
> college
```
4)This command also gives us where the two files are different and in what manner .
5)Enter grep /challenge/decoys_only.txt /challenge/decoys_and_real.txt 
``` bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
83a84
> pwn.college{QQUMVd7vLifbl1i0yIXWH8QzuBL.01MwMDOxwCNyUzNzEzW}
hacker@commands~comparing-files:~$
```
#What i learned
1)I learned how to use diff command and what is it is .
2)diff:The diff command is a essential command for comparing the contents of two files or directories. Its importance is efficiently identify 
and display the differences between versions of text-based data , and where the difference is located.

#References
I learnt basically to this this challenge from the explanation given in the challenges.










