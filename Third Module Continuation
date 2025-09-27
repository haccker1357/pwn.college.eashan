## Comprehending Commands
This is the third module in the Linux Luminarium .
This challenge contains 14 challenges .
6) Listing Files .
7) Touching Files .
8) Removing Files .
9) Moving Files .
10) Hidden Files .
11) An Epic File System Quest .
12) Making Directories .
13) Finding Files .
14) Linking Files .

 ## Listing Files 
In this challenge we need to find the name of the file which has the flag through the ls ( listing ) command .

 **Flag**
pwn.college{E8zPg7cyvWxF1fIKtLvL9pTKshx.QX4IDO0wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2) We need to list the files in the /challenge to fined the name of the ( /challenge/run ).
3)To list the files we need to use the listing ( ls ) command .
4) Enter ls /challenge in the terminal to find the name .
5) After finding the name run ( /challenge/( name ) ) in the terminal to secure the flag .
''' bash 
Connected!
hacker@commands~listing-files:~$ ls /challenge
24173-renamed-run-18287  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/24173-renamed-run-18287
Yahaha, you found me! Here is your flag:
pwn.college{E8zPg7cyvWxF1fIKtLvL9pTKshx.QX4IDO0wCNyUzNzEzW}
hacker@commands~listing-files:~$
'''
6) Copy and Paste the flag in the pwn.college website to complete the challenge .

# What i learned
1)What is ( ls ) command and how to use it .
ls : The ls command in Linux is a command used to list the contents of directories. When executed without any arguments, it displays the files and subdirectories 
within the current working directory.
2) Structure : ls ( Absolute path or Argument ) .

# Touching Files
In this challenge we need to create two files and run /challenge/run to get the flag .

**Flag**
pwn.college{YXTSn7VWz1fVOcnmAz88SFPV9PR.QXwMDO0wCNyUzNzEzW}

# Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2) We need to create two files ( /tmp/pwn and /tmp/college ) using ( touch ) command .
4) Then run ( /challenge/run ) to secure the flag .
''' bash 
Connected!
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ ls
bin  hsperfdata_root  tmp.TpSOPGOVKK
hacker@commands~touching-files:/tmp$ touch /tmp/pwn
hacker@commands~touching-files:/tmp$ touch /tmp/college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{YXTSn7VWz1fVOcnmAz88SFPV9PR.QXwMDO0wCNyUzNzEzW}
hacker@commands~touching-files:/tmp$
'''
5) Copy and Paste the flag in the pwn.college website to complete the challenge .

##What i Learned
1) What is ( touch ) command and how to use it .
touch : The touch command is used to create new, empty files .
2) Structure : touch (the name of the file we need to create) .

# Removing Files
In this challenge we need to remove files .

**Flag**
pwn.college{o0n4CQCb3xJqidm6lgjq1X5Crzu.QX2kDM1wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)We need to first create a new file named ( delete_me ) using the touch command .
3)After creating the file we need to delete that file which we created using ( rm ) command .
5) Then run ( /challenge/check ) to check if we created and deleted the file and then provide us with the flag .
''' bash 
Connected!
hacker@commands~removing-files:~$ touch delete_me
hacker@commands~removing-files:~$ ls
a  catflag  college  delete_me  flag  not-the-flag
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{o0n4CQCb3xJqidm6lgjq1X5Crzu.QX2kDM1wCNyUzNzEzW}
hacker@commands~removing-files:~$
'''
6) Copy and Paste the flag in the pwn.college website to complete the challenge .

#What i Learned
1)What is ( rm ) command annd how to use that command .
rm : The rm command in Linux is used to remove files or directories from the filesystem. It stands for "remove."
2) Structure : rm (the name of the file we nned to remove ) .

## Moving Files
In this challenge we need to move the /flag file into /tmp/hack-the-planet and the check it .

 **Flag**
pwn.college{AUnj-sAQ21Xi_vR7iw0d1-OdMvJ.0VOxEzNxwCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2) We need to move the file( /flag ) into ( /tmp/hack-the-planet ) using the ( mv ) command .
3)After moving we need to run /challenge/check to check if had moved it or not and then give our flag .

''' bash 
Connected!
hacker@commands~moving-files:~$ ls
a
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{AUnj-sAQ21Xi_vR7iw0d1-OdMvJ.0VOxEzNxwCNyUzNzEzW}

hacker@commands~moving-files:~$

4) Copy and Paste the flag in the pwn.college website to complete the challenge .

#What i Learned
1) What is mv command and how to use it .
mv : It relocates files or directories from one location to another within the filesystem.
Function : When moving files between different filesystems, mv typically copies the file to the destination and then deletes the original.
2)Structure : mv (name of the file we need to move ) (name of the place to where we need to move the file .)
In absolute paths .

# Hidden Files
In this challenge we learn how to see the hidden files in the file . Which cannot be seen by the ls command .

**Flag**
pwn.college{AxsQTfkeYJTEe5ubO7egdKif4oB.QXwUDO0wCNyUzNzEzW}
#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2) We need to change the directory from ~ to / as given .
3) Then use the command ( ls -a ) to show the hidden files in the directory .
5) After reading all the hidden files cat the file we need to secure the flag .
''' bash 
hacker@commands~hidden-files:~$ cd
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv          bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-134508076394  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-134508076394
pwn.college{AxsQTfkeYJTEe5ubO7egdKif4oB.QXwUDO0wCNyUzNzEzW}
hacker@commands~hidden-files:/$
'''
6) Copy and Paste the flag in the pwn.college website to complete the challenge .

 # What i Learned
1) We cannot see every file in the directory using the ( ls  ) command . Some files can be hidden .
2) What is ( ls - a ) command and how to use it .
ls -a : The ls -a command is used to list the hidden along with non hidden information about files and directories in the current directory .
3)Structure : ls (The file in which we want to read the hidden files .

## An Epic File System Quest
In this this challenge we need to use our total knowledge we learned till now to secure the flag .

**Flag**
pwn.college{cVNhuIYZCTtEXGSXMwpY9wqGePa.QX5IDO0wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2) We need to use all our knowledge we have learnt till now to get tha flag and comple the challenge .
''' bash
Connected!
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
POINTER  bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~an-epic-filesystem-quest:/$ cat POINTER
Congratulations, you found the clue!
The next clue is in: /usr/lib/emacsen-common/packages/install
The next clue is *hidden* --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/lib/emacsen-common/packages/install
hacker@commands~an-epic-filesystem-quest:/usr/lib/emacsen-common/packages/install$ ls
cmake-data  dictionaries-common  emacsen-common
hacker@commands~an-epic-filesystem-quest:/usr/lib/emacsen-common/packages/install$ ls -a
.  ..  .MEMO  cmake-data  dictionaries-common  emacsen-common
hacker@commands~an-epic-filesystem-quest:/usr/lib/emacsen-common/packages/install$ cat MEMO
cat: MEMO: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/emacsen-common/packages/install$ cat .MEMO
Yahaha, you found me!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/feature/lsmod/pretty/2
hacker@commands~an-epic-filesystem-quest:/usr/lib/emacsen-common/packages/install$ cd /opt/busybox/busybox-1.33.2/include/config/feature/lsmod/pretty/2
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/lsmod/pretty/2$ ls
6  BRIEF
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/lsmod/pretty/2$ cat BRIEF
Great sleuthing!
The next clue is in: /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/lsmod/pretty/2$ cd /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern$ ls
Alphabets  DoubleStruck  Latin  Marks  Monospace   Normal     README     Script  Size1  Size3  Size5  Size7    Variants           fontdata.js
Arrows     Fraktur       Main   Misc   NonUnicode  Operators  SansSerif  Shapes  Size2  Size4  Size6  Symbols  fontdata-extra.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern$ cat README
Tubular find!
The next clue is in: /usr/lib/ruby/gems/2.7.0/gems/irb-1.2.1/exe

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern$ cat /usr/lib/ruby/gems/2.7.0/gems/irb-1.2.1/exe
cat: /usr/lib/ruby/gems/2.7.0/gems/irb-1.2.1/exe: Is a directory
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern$ ls /usr/lib/ruby/gems/2.7.0/gems/irb-1.2.1/exe
CUE-TRAPPED  irb
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern$ cat CUE-TRAPPED
cat: CUE-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern$ ls -a CUE-TRAPPED
ls: cannot access 'CUE-TRAPPED': No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern$ ls -a /usr/lib/ruby/gems/2.7.0/gems/irb-1.2.1/exe.  ..  CUE-TRAPPED  irb
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern$ cat /usr/lib/ruby/gems/2.7.0/gems/irb-1.2.1/exe/CUE-TRAPPED
Tubular find!
The next clue is in: /opt/linux/linux-5.4/drivers/crypto/mediatek

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Latin-Modern$ cd /opt/linux/linux-5.4/drivers/crypto/mediatek
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ ls
ALERT  Makefile  mtk-aes.c  mtk-platform.c  mtk-platform.h  mtk-regs.h  mtk-sha.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ ls -a
.  ..  ALERT  Makefile  mtk-aes.c  mtk-platform.c  mtk-platform.h  mtk-regs.h  mtk-sha.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ cat ALERT
Great sleuthing!
The next clue is in: /usr/lib/python3/dist-packages/hyperlink

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ ls /usr/lib/python3/dist-packages/hyperlink
SECRET-TRAPPED  __init__.py  __pycache__  _url.py  test
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ cat SECRET-TRAPPED
cat: SECRET-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ ls /usr/lib/python3/dist-packages/hyperlink/SECRET-TRAPPED
/usr/lib/python3/dist-packages/hyperlink/SECRET-TRAPPED
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ ls /usr/lib/python3/dist-packages/hyperlink
SECRET-TRAPPED  __init__.py  __pycache__  _url.py  test
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ ls /usr/lib/python3/dist-packages/hyperlink/__init__.py
/usr/lib/python3/dist-packages/hyperlink/__init__.py
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ ls /usr/lib/python3/dist-packages/hyperlink/_url.py
/usr/lib/python3/dist-packages/hyperlink/_url.py
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ cat /usr/lib/python3/dist-packages/hyperlink/SECRET-TRAPPED
Tubular find!
The next clue is in: /opt/linux/linux-5.4/net/ipv4/bpfilter

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ ls /opt/linux/linux-5.4/net/ipv4/bpfilter
Makefile  SNIPPET-TRAPPED  sockopt.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ cat /opt/linux/linux-5.4/net/ipv4/bpfilter/Makefile
# SPDX-License-Identifier: GPL-2.0-only
obj-$(CONFIG_BPFILTER) += sockopt.o
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ cat /opt/linux/linux-5.4/net/ipv4/bpfilter/SNIPPET-TRAPPED
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/arch/arm/net

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ ls /opt/linux/linux-5.4/arch/arm/net
Makefile  TRACE-TRAPPED  bpf_jit_32.c  bpf_jit_32.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ cat /opt/linux/linux-5.4/arch/arm/net/Makefile
# SPDX-License-Identifier: GPL-2.0-only
# ARM-specific networking code

obj-$(CONFIG_BPF_JIT) += bpf_jit_32.o
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$ cat /opt/linux/linux-5.4/arch/arm/net/TRACE-TRAPPED
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{cVNhuIYZCTtEXGSXMwpY9wqGePa.QX5IDO0wCNyUzNzEzW}
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/crypto/mediatek$
'''
3)Copy and Paste the flag in the pwn.college website to complete the challenge .

# What i Learned
1) In this challenge i learnt that all challenges we facce are hard and not as easy as the previous challenge .

## Making Directories 
In this challenge we need to create a directory and make a file in it .

**Flag**
pwn.college{wynaq56nQG44ZX3grmjRxVsgglu.QXxMDO0wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2) First we need to create a directory ( /tmp/pwn ) and then create a file (college) in it and then run ( /challenge/run ) .
3) First make a new directory ( /tmp/pwn ) using command ( mkdir ).
4) Then change the directory into the created directory using the cd command.
5)Then create a file ( college 0 in it .
6) And then run ( /challenge/run ) to get the flag .
''' bash
Connected!
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{wynaq56nQG44ZX3grmjRxVsgglu.QXxMDO0wCNyUzNzEzW}
hacker@commands~making-directories:/tmp/pwn$
'''
7)Copy and Paste the flag in the pwn.college website to complete the challenge .

# What i Learned
1)We need to know how make new directory which is used for any purpose .
2)I learned what is ( mkdir ) command and how it is used .
mkdir : The mkdir command in Linux is used to create new directories (also known as folders) in the file system.
3) Structure : mkdir argument(Name of the directory which we need to create ) .

## Finding Files
In this challenge we need to find the flag which is placed in some random directory under some random name .

**Flag**


## Linking Links
In this level we need to use the symlinks to get the flag.

**Flag**
pwn.college{g2y6bKhdaG28_SDJq3GfaMYs-S4.QX5ETN1wCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)We need to run /challenge/catflag to get the flag .

''' bash
Connected!
hacker@commands~linking-files:~$ /flag
bash: /flag: Permission denied
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{g2y6bKhdaG28_SDJq3GfaMYs-S4.QX5ETN1wCNyUzNzEzW}
'''
3)Copy and Paste the flag in the pwn.college website to complete the challenge .

#What i Learned
1)I learned Types of Symbolic links .
Hard and Soft Link .
A soft link is a special type of file that contains the path to another file or directory
A hard link is a direct pointer to the inode of a file.



