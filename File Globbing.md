## File Globbing
This is the fifth Module in the Linux Luminarium.
This module contains 10 challenges.
1) Matching with * .
2) Matching with ? .
3) Matching with [] .
4) Matching paths with [] .
5) Multiple Globs .
6) Mixing Globs .
7) Exclusionary Globbing .
8) Tab Completion .
9) Multiple options for Tab Completion.
10) Tab Completion on commands.

## Matching with *
This challenge teaches about the glob ( * ) .

**Flag**
pwn.college{wZ3mm4x7HISedhCyqY_nEVpbEra.QXxIDO0wCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) We need to change the directory to /challenge with cd directory.
3) We need to use the ( * ) while changing the directory .
4) And the maximum number of characters are four .
5)Then we need to run /challenge/run .
```bash
Connected!
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{wZ3mm4x7HISedhCyqY_nEVpbEra.QXxIDO0wCNyUzNzEzW}
hacker@globbing~matching-with-:/challenge$
```
5)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1)When the terminal encounters a * character in any argument, the shell will treat it as a "wildcard" and try to replace that argument
with any files that match the pattern .
2)n Linux, the * glob  is a wildcard character used for pattern matching during filename expansion, a process known as globbing.

##
1) Matching with ? 
This challenge teaches about the glob ( ? ) .

**Flag**
pwn.college{gJkQZwU0Du9n07ctsFOpZHmX4Q1.QXyIDO0wCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) We need to change the directory to /challenge with cd directory.
3) We need to use the ( ? ) while changing the directory instead of c and l letters .
4) Enter cd /?ha??enge
5)Then we need to run /challenge/run .
``` bash
Connected!
This challenge resets your working directory to /home/hacker unless you change
directory properly...
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{gJkQZwU0Du9n07ctsFOpZHmX4Q1.QXyIDO0wCNyUzNzEzW}
hacker@globbing~matching-with-:/challenge$ 
```
6)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1)When it encounters a ? character in any argument, the shell will treat it as a single-character wildcard.
2)This works like *, but only matches one character.

##  Matching with []
This challenge teaches about the glob ( [] ) .

**Flag**
pwn.college{kcI8_P8BQhy2-diHExpzSbuhikl.QXzIDO0wCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) Run /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h
3)Enter /challenge/files$ /challenge/run file_[bash] .
``` bash
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{kcI8_P8BQhy2-diHExpzSbuhikl.QXzIDO0wCNyUzNzEzW}
```
4)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1)The square brackets are, essentially, a limited form of ?, in that instead of matching any character, [] is a wildcard for some subset of potential characters,
specified within the brackets.
2)For example, [pwn] will match the character p, w, or n

## Matching paths with [] .
This challenge teaches about the glob ( [] ) .

**Flag**
pwn.college{cz4CWqigfYtaWpDtwVdh5rScbM4.QX0IDO0wCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)Run /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files.
3)Enter /challenge/run /challenge/files/file_[bash] .
``` bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ ls
file_a  file_c  file_e  file_g  file_i  file_k  file_m  file_o  file_q  file_s  file_u  file_w  file_y
file_b  file_d  file_f  file_h  file_j  file_l  file_n  file_p  file_r  file_t  file_v  file_x  file_z
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{cz4CWqigfYtaWpDtwVdh5rScbM4.QX0IDO0wCNyUzNzEzW}
hacker@globbing~matching-paths-with-:~$
```
4)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1)The square brackets are, essentially, a limited form of ?, in that instead of matching any character, [] is a wildcard for some subset of potential characters,
specified within the brackets.
2)Globbing happens on a path basis, so you can expand entire paths with your globbed arguments.

## Multiple Globs 
This challenge teaches about how to use multiple globs at the same time unlike the previous challenges which use one glob at a time .

**Flag**
pwn.college{AOsgJRcGTt6okDOvlYn2_pqYx43.0lM3kjNxwCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)Bash supports the expansion of multiple globs in a single word.
3) We need to change the directory to /challenge/files with cd directory.
4)Run /challenge/run, providing a single argument .
5) With arguments 3 characters globbed word with two * globs in it that covers every word that contains the letter p.
6)Enter /challenge/run *p*
7) The * glob  is a wildcard character used for pattern matching during filename expansion .
``` bash
hacker@globbing~multiple-globs:~$ cd /challenge/files
globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{AOsgJRcGTt6okDOvlYn2_pqYx43.0lM3kjNxwCNyUzNzEzW}
hacker@globbing~multiple-globs:/challenge/files$
```
8)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) How to use Multiple globs at the same time with an example .

## Mixing Globs 
This challenge requires us to the previous knowledge gained on globs and use it to get the flag .

**Flag**
pwn.college{cqIJkQ_WiMFXGMQT2feh7m10Sv5.QX1IDO0wCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) We need to change the directory to /challenge/files with cd directory.
3)We need to pass an argument to /challenge/run to get the required the required files.
4)We need to have the argument short with 6 characters or less .
5) The argument is the first first letters of each required word .
6) We use the( * ) glob to fill the remaining word .
7)Enter /challenge/run [cep]*
``` bash
Connected!
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{cqIJkQ_WiMFXGMQT2feh7m10Sv5.QX1IDO0wCNyUzNzEzW}
hacker@globbing~mixing-globs:/challenge/files$
```
8) Copy and Paste the flag in the pwn.college website to complete the challenge.

# What i Learned
1) It is not sufficient to learn to use individual globs but we need to learn to use two or more of them at the same time.
2)From this challenge we learn to use two or more of them at the same time

## Exclusionary Globbing
This challenge teaches us how to filter out files from globs.

**Flag**
pwn.college{oqPiNnyeMfYYzWISmTZGKlbwQOx.QX2IDO0wCNyUzNzEzW}

 #Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) We need to change the directory to /challenge/files with cd directory.
3)We need to pass an argument to /challenge/run to get the required the required files.
4)We need to have the argument short with 8 characters or less .
5) The argument is the first first letters of each required word .
6)  We use the( ! ) glob to get the words without the first letters in the argument .
7) Enter /challenge/run file_[!pwn]
``` bash
Connected!
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run file_[!pwn]
Error: your argument is too long! It must be 8 characters or less.
hacker@globbing~exclusionary-globbing:/challenge/files$ ls
amazing    challenging  educational  great  incredible  kind      magical  optimistic  queenly  splendid   uplifting   wonderful  youthful
beautiful  delightful   fantastic    happy  jovial      laughing  nice     pwning      radiant  thrilling  victorious  xenial     zesty
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{oqPiNnyeMfYYzWISmTZGKlbwQOx.QX2IDO0wCNyUzNzEzW}
hacker@globbing~exclusionary-globbing:/challenge/files$
```
8) Copy and Paste the flag in the pwn.college website to complete the challenge.

##What i Learned
1)I learnt how to invert the the glob , to get the words that doesn`t start with the entered letters .
2)The ! character has a different special meaning in bash when it`s not the first character of a [] glob .
3) ^ does not have this problem.

# Tab Completion 
This challenge is about how to use the <tab> key .

**Flag**
pwn.college{Q2H71KMbEYT0jQjihVpFGD8trRJ.0FN0EzNxwCNyUzNzEzW}

 #Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)We need to use the <tab key>to complete the words we are trying to type, this is Auto-Completion .
3)Use the cat command for the argument /challenge/p then click <tab> .

``` bash
hacker@globbing~tab-completion:~$ ls /challenge
DESCRIPTION.md  pwncollege
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege
cat: /challenge/pwncollege: No such file or directory
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege
pwn.college{Q2H71KMbEYT0jQjihVpFGD8trRJ.0FN0EzNxwCNyUzNzEzW}
hacker@globbing~tab-completion:~$
,,,

4)Copy and Paste the flag in the pwn.college website to complete the challenge.

# What i learned
1)When we hit that tab key, the name will expand and you`ll be able to read the file.
2) If you hit tab in the shell, it`ll try to figure out what you`re going to type and automatically complete it. Auto-completion is super useful.

## Multiple options for Tab Completion.
This challenge is about how to use the <tab> key .

**Flag**
pwn.college{8BRRe_VBHpvHZ_GdMJP7fPsi_19.0lN0EzNxwCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)We need to use the <tab key>to complete the words we are trying to type, this is Auto-Completion .
3)Use the cat command for the argument /challenge/p then click <tab> .
4) By default bash will auto-expand until the first point when there are multiple options .
5) When you hit tab a second time, it`ll print out those options.
6) We need to change the directory to /challenge/files with cd directory.
``` bash
Connected!
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-flag
pwn.college{8BRRe_VBHpvHZ_GdMJP7fPsi_19.0lN0EzNxwCNyUzNzEzW}
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$
```
7) Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1)When we hit that tab key, the name will expand and you`ll be able to read the file.
2) If you hit tab in the shell, it`ll try to figure out what you`re going to type and automatically complete it. Auto-completion is super useful.

##  Tab Completion on commands
This challenge is about how to use the <tab> key .

**Flag**
pwn.college{Ut6gVLlLdWqtPT5zbm-uqCBd3tb.0VN0EzNxwCNyUzNzEzW}

#Process
1)First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)We need to use the <tab key>to complete the words we are trying to type, this is Auto-Completion .
3)We need type pwncollege and enter<tab> for completion of the argument.
4)After appearing the code click Enter.
``` bash
Connected!
hacker@globbing~tab-completion-on-commands:~$ pwncollege-30765
.bash_history  .config/       .lesshst       a              catflag        college        flag           not-the-flag
hacker@globbing~tab-completion-on-commands:~$ pwncollege-30765
Correct! Here is your flag:
pwn.college{Ut6gVLlLdWqtPT5zbm-uqCBd3tb.0VN0EzNxwCNyUzNzEzW}
hacker@globbing~tab-completion-on-commands:~$
```
 5)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1)When we hit that tab key, the name will expand and you`ll be able to read the file.
2) If you hit tab in the shell, it`ll try to figure out what you`re going to type and automatically complete it. Auto-completion is super useful.

