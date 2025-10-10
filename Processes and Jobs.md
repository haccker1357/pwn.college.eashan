##Processes and Jobs
This is the ninth module in linux luminarium.
This module contains 10 challenges .
1) Listing Processes .
2) Killing processes .
3) Interrupting Processes .
4) Killing misbehaving Process .
5) Suspending Process.
6) Resuming Processes .
7) Backgrounding Processes .
8) Foregrounding Processes .
9) Starting Backgrounded Process .
10) Process Exit codes.

#Listing Processes
This challenge require us to list running processes and find the desired program .

**Flag**
pwn.college{cb_wOEwZqMMqh_npVJUs7vjmBuT.QX4MDO0wCNyUzNzEzW}

#Process 
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)We need to list every process running in the terminal, For this we need to use ps command . 
3) For making use of this ps command we need to pass some arguments.
4)There are two types of arguments ps -ef and ps aux which is "Standard" Syntax and "BSD" Syntax respectively .
5) In this challenge we can use ps -ef to list all the programs running an find which of the programs is the required one .
6)Enter  ps -ef
7) Then we can find the required program .
8)Enter /challenge/16602-run-1396 which will give the required flag .

``` bash
Connected!
hacker@processes~listing-processes:~$ ps
    PID TTY          TIME CMD
    137 pts/0    00:00:00 ssh-entrypoint
    143 pts/0    00:00:00 bash
    152 pts/0    00:00:00 ps
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 14:57 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-i
root           7       1  0 14:57 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 14:57 ?        00:00:00 /challenge/16602-run-13966
root         135     132  0 14:57 ?        00:00:00 sleep 6h
hacker       137       0  0 14:57 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       143     137  0 14:57 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       153     143  0 14:58 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/16602-run-13966
Yahaha, you found me! Here is your flag:
pwn.college{cb_wOEwZqMMqh_npVJUs7vjmBuT.QX4MDO0wCNyUzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```
9) Copy and Paste the flag in the pwn.college website to complete the challenge .

#What i Learned
1)How to list all the programs running in the terminal using the ps command .
2)And i learned about two types of arguments given to the command ps which are ps -ef and ps aux


# Killing processes
This challenge requies us terminate not required processes from the terminal .

**Flag**
pwn.college{QHhV2Hwens6iHxeC6S9RIjsdJ4W.QXyQDO0wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college

