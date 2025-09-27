## Digesting Documentation
This is the fourth module in the Linux Luminarium.
This module contains 7 challenges
1) Learning from Documentation .
2) Learning Complex Usage .
3)Reading Manuals .
4) Searching Manuals .
5) Searching  for Manuals .
6) Helpful Programs .
7) Help for Builtins .

#Learning from Documentation 
In this challenge we need to invoke a correct argument to get the flag.

**Flag**
pwn.college{cXfmpEf_VioldM-oMp7l12tJH0w.QX0ITO0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)As given we need to invoke a proper argument to get the flag.
3)We need to invoke --giveflag argument to the command /challenge/challenge .
''' bash 
Connected!
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{cXfmpEf_VioldM-oMp7l12tJH0w.QX0ITO0wCNyUzNzEzW}
hacker@man~learning-from-documentation:~$
'''
4)Copy and Paste the flag in the pwn.college website to complete the challenge.

# What i Learned 
1) The correct usage of programs depends, in a large part, on the proper specification of arguments to them. 
2) Structure: command argument

##Learning Complex Usage 
This challenge involves us to to give argument to an argument to print flag file.

**Flag**
pwn.college{ADhE_P_B7o-pXoKP5reJ6ZW1TaK.QX1ITO0wCNyUzNzEzW}

# Process
1) First  we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)As given we need to give an argument ( flag ) to an argument ( --printflag ) to secure the flag .
3) Enter /challenge/challenge( command ) --printfile flag .

''' bash
Connected!
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile
You must pass a file for --printfile to read!
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /challenge/DESCRIPTION.md
Correct argument! Here is the /challenge/DESCRIPTION.md file:
While using most commands is straightforward, the usage of some commands can get quite complex.
For example, the arguments to commands like `sed` and `awk`, which we're definitely not getting into right now, are entire programs in an esoteric programming language!
Somewhere on the spectrum between `cd` and `awk` are commands that take arguments to their arguments...

This sounds crazy, but you've already encountered this with the `find` level in [Basic Commands](/linux-luminarium/commands).
`find` has a `-name` argument, and the `-name` argument itself takes an argument specifying the name to search for.
Many other commands are analogous.

Here is this level's documentation for `/challenge/challenge`:

> Welcome to the documentation for `/challenge/challenge`! This program allows you to print arbitrary files to the terminal, when given the `--printfile` argument. The argument 
to the `--printfile` argument is the path of the flag to read. For example, `/challenge/challenge --printfile /challenge/DESCRIPTION.md` will print out the description of the level!
Given that documentation, go get the flag!
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile flag
Correct argument! Here is the flag file:
pwn.college{ADhE_P_B7o-pXoKP5reJ6ZW1TaK.QX1ITO0wCNyUzNzEzW}
hacker@man~learning-complex-usage:~$
'''
4)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) We can give arguments to arguments and to only some type of arguments .
2) I Learnt about the argument ( --printfile )
3) ( --printfile )can access and display the arguments passed to it on the command line.
5) Structure : command --printfile

## Reading Manuals
In this challenge we will learn how to know about the any command ( if we dont know ) using another command.

**Flag**
pwn.college{gAqMgPeb63XJzMtNc7zTmWl7-el.QX0EDO0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)We need to learn about the command ( challenge ) using the manual.
3)To learn using manual we need to use man command.
4)Enter man challenge to get manual.
5)After that we need to solve the secret option to get the flag.
''' bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge - print the flag
Incorrect usage! Please read the challenge man page!
hacker@man~reading-manuals:~$ /challenge/challenge --gqgebz 637
Correct usage! Your flag: pwn.college{gAqMgPeb63XJzMtNc7zTmWl7-el.QX0EDO0wCNyUzNzEzW}
hacker@man~reading-manuals:~$
'''
6)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1)We learnt about how to learn about a command if we dont know about it.
by using ( man ) command.
man : The man command in Linux provides access to the system's manual pages, which are comprehensive documentation for commands, functions,  a
vailable in the operating system. These manual pages, often called "man pages," serve as an on-board reference guide for users.
2)Structure: man (command)

# Searching Manuals
This challenge requires us to find the option that gives us the flag .

**Flag**
pwn.college{gsk-7Ox8irUSGrFbPUYHcHU3Aez.QX1EDO0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)As the previous challenge we need to learn about the command ( challenge ) using the manual.
3) Enter man challenge to get manual.
4) After that we need to solve the secret option to get the flag.
Connected!
hacker@man~searching-manuals:~$ man challenge      
hacker@man~searching-manuals:~$ /challenge/challenge --xd
Initializing...
Correct usage! Your flag: pwn.college{gsk-7Ox8irUSGrFbPUYHcHU3Aez.QX1EDO0wCNyUzNzEzW}
hacker@man~searching-manuals:~$
'''
5) Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1)We learnt about how to learn about a command if we dont know about it.
by using ( man ) command.
man : The man command in Linux provides access to the system's manual pages, which are comprehensive documentation for commands, functions,  a
vailable in the operating system. These manual pages, often called "man pages," serve as an on-board reference guide for users.
2) Structure: man (command)

## Helpful Programs
This challenge requires us to learn about the argument if a man page is not available .

**Flag**
pwn.college{YQhG_u7OI8epKNC-XpC4aPEaZlL.QX3IDO0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2) We need to use command( /challenge/challenge ) with an argument .
3)As an man page is not available on /challenge/challenge we need to use ( --help ) as an argument.
4)Enter /challenge/challenge for intial steps.
5)Then we need to decode the secret and secure the flag .
''' bash
Connected!
hacker@man~helpful-programs:~$ challenge --help
bash: challenge: command not found
hacker@man~helpful-programs:~$ help challenge
bash: help: no help topics match `challenge'.  Try `help help' or `man -k challenge' or `info challenge'.
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]                                                                       
optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flagWW
hacker@man~helpful-programs:~$ /challenge/challenge -p                           
The secret value is: 784                                                                              
hacker@man~helpful-programs:~$ /challenge/challenge -g 784
Correct usage! Your flag: pwn.college{YQhG_u7OI8epKNC-XpC4aPEaZlL.QX3IDO0wCNyUzNzEzW}
hacker@man~helpful-programs:~$
'''
6)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1)There are some commands which do not have a man page ,these commands require an argument (--help ) to know about them .
2)We learnt about ( --help )argument and how to use it .
3)The --help argument in Linux is  used to display a brief summary of a command's usage, 
available options (flags), and a short description of what the command does.
4)It is a quick and easy way to get information about how to use a specific command without needing to consult external documentation or man pages.
5) Structure : command --help

## Help for Builtins
This challenge teaches us about builtins.

**Flag**
pwn.college{c7ULs_5IrBWGKJCUAm4IO_xEssF.QX0ETO0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2) Some commands, rather than being programs with man pages and help options, are built into the shell itself. These are called builtins.
3)To learn about these commands we need an help command .
4)This challenge's challenge command is a shell builtin, rather than a program.
5)Enter help challenge to learn about that command .
6)After we need to decode the secret to get the flag .
''' bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "c7ULs_5I".
hacker@man~help-for-builtins:~$ challenge --secret c7ULs_5I
Correct! Here is your flag!
pwn.college{c7ULs_5IrBWGKJCUAm4IO_xEssF.QX0ETO0wCNyUzNzEzW}
hacker@man~help-for-builtins:~$
'''
7) Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) There are some commands which are built into the shell itself .
to assess about these command we take the help of the builtin help .
2)Struture : help (builtin)
