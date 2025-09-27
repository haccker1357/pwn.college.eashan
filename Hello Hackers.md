#First Module in Linux Luminarium

## Hello Hackers
This module contains three challenges.
  1) Intro to Commands.
  2) Intro to Arguments.
  3) Command History.

## Intro to Commands 
In this challenge, i need to invoke the hello command to get the flag!

## My Solution
**Flag** 
pwn.college{oJvMXikGflXl-Kb6TtepfDrIyiP.QX3YjM1wCNyUzNzEzW}
1) I linked my ubuntu terminal to the pwn.college dojo using public ssh key which I generated using `cat key.pub`

2) Then I connected the required challenge ( Intro to commands) using ssh command in the terminal
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
Now it is Connected to the terminal.

3) Open the terminal and after understanding the challenge, that is type `hello` and click enter. We will get the flag that is needed and for completing the challenge we need 
to submit the flag in  the given location and then it will show as Solved ` Intro to Commands`.
``` bash
hacker@hello~intro-to-commands:~$ hello
Success! Here is your flag:
pwn.college{oJvMXikGflXl-Kb6TtepfDrIyiP.QX3YjM1wCNyUzNzEzW}
```

I read the instructions given in the challenge and noticed that we need to invoke the command hello.

## What I Learned 
1) hacker@dojo:~$
This is called the "prompt", and it`s prompting us to enter an command.
2)Once we enter the command and click enter ,the command will be executed and a new prompt will open waiting for the next command.
3)Commands in Linux are case sensitive: hello is different from HELLO.
4)After every command we need to click enter key to run it .
5)How to launch a terminal and how and what a command is.
 Command: It is a insturuction given by the user in the terminal to perform a specific task.

## Intro to Arguments 
In this challenge, to get the flag, you must run the hello command with an 
argument of hackers.

**Flag** 
pwn.college{sCavsXAIzFTc2DSwGwJkpN-aT4a.QX4YjM1wCNyUzNzEzW}

1) I linked my ubuntu terminal to the pwn.college dojo using public ssh which I generated using `cat key.pub`

2) Then I connected the required challenge ( Intro to Arguments) using ssh command 
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
Now it is Connected to the terminal.

3) Open the terminal and after understanding the challenge, type `hello hackers` 
( command+ argument ) and click enter. We will get the flag that is needed and for completing the challenge we need to submit the flag in the given location and then a 
pop up opens with text Solved `Intro to Arguments`.
``` bash
hacker@hello~intro-to-arguments:~$ hello hackers
Success! Here is your flag:
pwn.college{sCavsXAIzFTc2DSwGwJkpN-aT4a.QX4YjM1wCNyUzNzEzW}
```

I read the instructions given under the challenge and noticed that we need to invoke the command hello along with the argument hackers as the name of the challenge suggests.

## What I Learned 
1)I learned the Command+Argument structure from this challenge.
2)`echo` is a simple command that "echoes" all of its arguments back out onto the terminal.
Example :hacker@dojo:~$ echo hello hackers
hello hackers
3) We can use echo command for multiple arguments.
4) How to launch a terminal and what is an argument and how to use it.
Arguments : Arguments are the inputs provided to a command in the terminal. They modify the command`s behavior .

## Command History
In this Challenge we need to bring up the last command we used in the terminal.By doind this challenge we get the flag that is in the command history.

*Flag* 
pwn.college{cTCxtOPaui5C1tIOfTDJIKLzfbX.0lNzEzNxwCNyUzNzEzW}
1) I linked my ubuntu terminal to the pwn.college dojo using public ssh which I generated using `cat key.pub`.

2) Then I connected the required challenge ( Command History ) using ssh command 
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
Now it is Connected to the terminal.

3) Open the terminal and after understanding the challenge, type `hello hackers` 
( command+ argument ) and click enter. We will get the flag that is needed and for completing the challenge we need to submit the flag in the given location and then a 
pop up opens with text Solved `Command History`
```bash
Connected!
hacker@hello~command-history:~$ the flag is pwn.college{cTCxtOPaui5C1tIOfTDJIKLzfbX.0lNzEzNxwCNyUzNzEzW

Success! Here is your flag

I read the instructions given under the challenge and noticed that we need to click the up arrow key in our keyboard to access the previous command.

## What I Learned 
1)I can assess the previous command by clicking the up arrow key in our keyboard.
2)We can assess the whole history but once at a time by clicking the up arrow key in our keyboard as many times we want , the command appears after the prompt.
3) This helps us to remember the previous commands of what we have used or check out large commands that we have used.
4) How to launch a terminal and how to retrieve the previous command we used .

## Referenceces
I listened and learnt from the videos that are given in the pwn.college website by Hacker Yan.
The Video is ( https://www.youtube.com/watch?v=g_85EVO3IC0 )

