## Shell Variables
This is the seventh module in the Linux Luminarium.
This module contains 8 challenges.
1) Printing Variables
2) Setting Variable
3) Multi word Variables
4) Exporting Variables
5) Printing Exported Variables
6) Storing Command Output
7) Reading input
8) Reading Output

## Printing Variables
This challenge requires us to pront a variable.

**Flag**
pwn.college{QGid71ds8_wWc_SreV81SKedpZ7.QX3UTN0wCNyUzNzEzW

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)We need to print variables with the echo command too.
3) But we must prepend the variable name with a $ character.
4) Enter echo $FLAG

``` bash
Connected!
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{QGid71ds8_wWc_SreV81SKedpZ7.QX3UTN0wCNyUzNzEzW}
hacker@variables~printing-variables:~$
```
5)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) How to print the value in the variable.
2) Structure:echo $Name

##Setting Variable
This challenge requires us to assign values to variables.

**Flag**
pwn.college{Q2SvPVcgG4NDmNOJ_goAI0UOzl3.QX5UTN0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) Even can assign values to Variables.
3) To do we need to equate the Name of variable to the value we want to assign.
4) Enter PWN=COLLEGE.This will print the required flag.

``` bash
Connected!
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Q2SvPVcgG4NDmNOJ_goAI0UOzl3.QX5UTN0wCNyUzNzEzW}
hacker@variables~setting-variables:~$ echo $PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Q2SvPVcgG4NDmNOJ_goAI0UOzl3.QX5UTN0wCNyUzNzEzW}
hacker@variables~setting-variables:~$
```
5)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) How to assign values to a variable and how to read them.
2)Structure: (Variable name)=(Value)

##Multi word Variables 
This challenge requires us yo assign more than one value to a variable at he same time.

**Flag**
pwn.college{4fqTdIs3jjDGXlGN3osjDaH1Epc.QXwYTN0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) We can not only assign only one value to variable at the same time but more .
3) When the shell sees a space, it ends the variable assignment and interprets the next word as a command.
4) For this we need to keep the value in a closed "value" .
5)Enter PWN="COLLEGE YEAH"

``` bash
Connected!
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{4fqTdIs3jjDGXlGN3osjDaH1Epc.QXwYTN0wCNyUzNzEzW}
hacker@variables~multi-word-variables:~$ echo $PWN
COLLEGE YEAH
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{4fqTdIs3jjDGXlGN3osjDaH1Epc.QXwYTN0wCNyUzNzEzW}
hacker@variables~multi-word-variables:~$
```
6) Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) How to assign more than one value to a variable at the same time.
2) Structure : NAME="Value"

##Exporting Variables 
This challenge teaches us how go export an Variable.

**Flag**
pwn.college{c56jN2wg_c9Gptaz8Lz4aI75gtB.QXyYTN0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)By default, variables that you set in a shell session are local to that shell process.
3)The other commands you run doesn't inherit them .
4)To export these variables we need to use the command export.
5) We need to assign the value COLLEGE to variable PWN and export it.
6) Then we need to create the variable COLLEGE with value PWN.
7)Enter export PWN=COLLEGE and COLLEGE=PWN
8) Then ruh the command /challenge/run

```  bash
Connected!
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{c56jN2wg_c9Gptaz8Lz4aI75gtB.QXyYTN0wCNyUzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$
```
9)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) How to export a variable to the environment.
2) Structure : export NAME
we can the export and assign a value to the Variable at the same time 
Structure: export NAME=VALUE

##Printing Exported Variable 
This challenge requires us to Print an exported variable .

*Flag**
pwn.college{8-DOG7c_UpJVb_sW00bfC4EE20z.QX4UTN0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) To print every exported variable in the shell we need to use env command.
3) Then we need to find the flag in the list of exported variables.
4)Enter env

``` bash
Connected!
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=c425b9657496010c9090138efaf3297eb5ef30e1ff2eb8b5b46a99e3c62ea873
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{8-DOG7c_UpJVb_sW00bfC4EE20z.QX4UTN0wCNyUzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
hacker@variables~printing-exported-variables:~$
```
5)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) How to print every exported variable in the shell.

## Reading input
This challenge requires us to read a variable.

**Flag**
pwn.college{gw97vGa4lhhAG87cUUN_ZFenIF-.QX4cTN0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) Read reads data from your standard input.
3) read -p argument, which lets you specify a prompt.
4) For reading the variable we need to use read -p .
5) Enter read -p "INPUT: " PWN

``` bash
Connected!
hacker@variables~reading-input:~$ read -p "INPUT: " PWN
INPUT: COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{gw97vGa4lhhAG87cUUN_ZFenIF-.QX4cTN0wCNyUzNzEzW}
hacker@variables~reading-input:~$
```
6)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) How to Read a variable.
2) Using the -p argument, which lets you to specify a prompt and read only that.
3) The read reads data from your standard input,

## Reading files
This challenge requires us to read files.

**Flag**
pwn.college{ohR3VNtBn9-OCfRM-cZ_Js4vvFC.QXwIDO0wCNyUzNzEzW}

# Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) We need to redirect the output of the /challenge/run to the variable.
3)Then read the variable ,it will give us the required flag.
4) Enter read PWN < /challenge/read_me

``` bash
Connected!
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{ohR3VNtBn9-OCfRM-cZ_Js4vvFC.QXwIDO0wCNyUzNzEzW}
hacker@variables~reading-files:~$
'''
5)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) How to read a file into an environment variable .
2) How to redirect files inro the the variables .

























