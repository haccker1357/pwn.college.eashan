##Untangling Users
This is the tenth module in the Linux Luminarium .
This module contains four challenges.
1)Becoming root with su .
2) Other users with su .
3) Cracking Passwords .
4) Using SUDO .

#Becoming root with su
This challenges require us to have the root access .

**Flag**
pwn.college{YAwgipZneHk6NCLNANDfrcnfYzh.QX1UDN1wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2) In this challenge we need to elevate to root access using the su command, which is generally sused in the past.
3)We need to switch user and then read the flag , This will give us the required flag .
4)First enter su , This will prompt us to give password.
5)After entering the given password the user will be switched to the root .
6)This will allow user to have the privilages of the administrtor .
7)Then Enter cat /flag toread the desired flag.

``` bash
Connected!
hacker@users~becoming-root-with-su:~$ su
Password:
su: Authentication failure
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{YAwgipZneHk6NCLNANDfrcnfYzh.QX1UDN1wCNyUzNzEzW}
root@users~becoming-root-with-su:/home/hacker#
```
8)Copy and Paste the flag in the pwn.college website to complete the challenge .

#Wh
