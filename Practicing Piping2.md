## Practicing Piping
This is the sixth module in the linux luminarium.
This challenge contains 14 challenges.
5) Redirecting input .
6) Grepping stored results .
7) Grepping live output .
8) Grepping errors .
9) Flitering with grep -v .
10) Duplicating piped data with tee .
11) Process substitution for input .
12) Writing to multiple programs .
13) Split piping stderr and stdout
14) Named Pipes .


## Redirecting input
This challenge shows how to redirect the input to programs as we did with the output and error.

**Flag**
pwn.college{8RCHCxV1Tr8jAOBKElAvZMAioHE.QXwcTN0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) First we need to write the value COLLEGE to PWN file.
3) Enter echo COLLEGE > PWN
4) Then we need to redirect the PWN file to /challenge/run using the stdin character ( < )
5) Enter /challenge/run < PWN

``` bash
Connected!
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{8RCHCxV1Tr8jAOBKElAvZMAioHE.QXwcTN0wCNyUzNzEzW}
hacker@piping~redirecting-input:~$
``` 
4)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i learned
1) How to redirect the input to the program like how did we do with the output and error.
2)The the stdin character we use for this redirection is ( < )

## Grepping Stored results
This challenge requires us to use both the stdout character and the grep command .

**Flag**
pwn.college{8atqKaJbr_m_LXSIWQfPf0InwwY.QX4EDO0wCNyUzNzEzW}

# Process 

1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) First we need to redirect the stdout of /challenge/run to the /tmp/data.txt .
3)/challenge/run > /tmp/data.txt
4) After Confirmation grep through the output to find the desired falg through the keyword.
5) Enter grep pwn.college /tmp/data.txt

``` bash
Connected!
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep flag /tmp/data.txt
[FLAG] Here is your flag:
flagon
camouflaging
flagged
flagella
conflagration
flagstaff
flagstone
flagellating
flagellum's
flagpole's
camouflages
camouflage
conflagration's
camouflage's
flagship's
flagellates
flagstaffs
flagstaff's
flagstones
flagellum
camouflaged
flagging
flagons
conflagrations
flags
flagrant
flagellation
flagon's
flagship
persiflage's
flagellated
flagellate
unflagging
flagpole
flag
flagpoles
flagships
flagellation's
flagstone's
flagellums
flag's
persiflage
flagrantly
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{8atqKaJbr_m_LXSIWQfPf0InwwY.QX4EDO0wCNyUzNzEzW}
hacker@piping~grepping-stored-results:~$
```

6) Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) How to direct the output to a file.
2) How to find the required result through the grep command.

## Grepping live output
This challenge teaches us how to use the pipe operator.

**Flag**
pwn.college{oiHlKAM_oKRJ9yu_Rse3Nvn4IR_.QX5EDO0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) To avoid the need to store results to a file we need to use the pipe operator ( | ).
3) Redirect the output of /challenge/run aand grep through the output to findvthe flag.
4) Enter. /challenge/run | grep pwn.college
5) After confirmation it will print out the flag.

``` bash
Connected!
hacker@piping~grepping-live-output:~$ grep pwn.college /challenge/run
#!/opt/pwn.college/bash
hacker@piping~grepping-live-output:~$ /challenge | grep pwn.college
bash: /challenge: Is a directory
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{oiHlKAM_oKRJ9yu_Rse3Nvn4IR_.QX5EDO0wCNyUzNzEzW}
hacker@piping~grepping-live-output:~$
```

6) Copy and Paste the flag in the pwn.college website to complete the challenge.

# What i learned
1)Standard output from the command to the left of the pipe will be connected to (piped into) the standard input of the command
to the right of the pipe. 
2)To avoid the need to store results to a file we need to use the pipe operator and it also cut the middle man.

## Grepping Error
This challenge requires to redirect the stdout and stderr and grep through the stderr to secure the flag.

**Flag**
pwn.college{w9ZV0mU-Tgp-lKlZcYCiddKRIje.QX1ATO0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) First  we need to redirect standard error to standard output (2>& 1) .
3) Then pipe the now-combined stderr and stdout as normal (|) pipe operator .
4) Enter /challenge/run 2>&1 | grep pwn.college
5) Afte Conformation it will print out the flag.

``` bash
Connected!
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{w9ZV0mU-Tgp-lKlZcYCiddKRIje.QX1ATO0wCNyUzNzEzW}
hacker@piping~grepping-errors:~$
```
6)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) How to grep through the errors directly.
2) How to redirect standard error to standard output using (2>& 1) character.

## Filtering with grep -v
This challenge shows how to filter out the data we don't want to the required data.

**Flag**
pwn.college{wjc2dvhETzNZ68MTjl0EpqdFlEl.0FOxEzNxwCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) To get the data we want we need to filter out the data we don't need.
3) For this we can use the invert grep command ( grep -v ) .
4) Enter /challenge/run | grep -v DECOY
5) Then all the data containing the keyword DECOY is filtered out.
``` bash
Connected!
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{wjc2dvhETzNZ68MTjl0EpqdFlEl.0FOxEzNxwCNyUzNzEzW}
hacker@piping~filtering-with-grep-v:~$
```
6) Copy and Paste the flag in the pwn.college website to complete the challenge.

# What i learned
1) The only way to filter to just the data you want is to filter out the data you don't want.
2) To do this we nuse the invert grep command ( grep -v ).
3) Structure: grep -v keyword.
It will print all the words without the keyword .


## Duplicating piped data with tee
This challenge teaches how to duplicate data flowing through your pipes to any number of files provided on the command line.

**Flag**
pwn.college{IYo8QWR77BBJAx2wt72cH7qRZAe.QXxITO0wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
``` command
2) To duplicate the stdout from /challenge/pwn to/challenge/college  we need to use the tee command .
3) By using the tee command it will show you the output .
4)Enter /challenge/pwn | tee pwn_code | /challenge/college.
5) Then using the given output secure the flag .

``` bash
Connected!
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn_code | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn_code
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "IYo8QWR7"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret IYo8QWR7 | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{IYo8QWR77BBJAx2wt72cH7qRZAe.QXxITO0wCNyUzNzEzW}
hacker@piping~duplicating-piped-data-with-tee:~$
```
6) Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned 
1) By providing two files to tee, we ended up with three copies of the piped-in data: one to stdout, one to the pwn file, and one 
to the college file.
2) Using tee command, named after a "T-splitter" from plumbing pipes, duplicates data flowing through your pipes to any
 number of files provided on the command line. 

## Process substitution for input
This challenge requirea us to compare to commands.

**Flag**
pwn.college{oYZzf13xhXuQ7f3eSOxfKNmvDfj.0lNwMDOxwCNyUzNzEzW}

 # Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) We learnt how tocompare two files using diff command.
3) But rwo compare two command we need to turn them into temporary files and then compare them.
4) To turn them into temporary files we need to write them in <(command) .
5) By running ,the bash will run the command and transfer its output to a temporary file that it will create. 
6) Enter diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)

``` bash
Connected!
hacker@piping~process-substitution-for-input:~$ echo <(diff /challenge/print_decoys /challenge/print_decoys_and_flag)
/dev/fd/63
hacker@piping~process-substitution-for-input:~$ cat <(diff /challenge/print_decoys /challenge/print_decoys_and_flag)
5c5
< cat /challenge/.decoys_only
---
> cat /challenge/.decoys_and_real
hacker@piping~process-substitution-for-input:~$ cat /dev/fd/63
cat: /dev/fd/63: No such file or directory
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
38a39
> pwn.college{oYZzf13xhXuQ7f3eSOxfKNmvDfj.0lNwMDOxwCNyUzNzEzW}
hacker@piping~process-substitution-for-input:~$
```
7)Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
1) How to read a command by making it a temporary file by transferring the output to the temporary file.
2) By writing the command in <(command) this is called Process Substitution.
3) How to compare commands by creating them into temporary files .

##Writing to Multiple Programs
This challenge requires us to duplicate the data to two commands using tee command.

**Flag**
pwn.college{cy-8f2HUX91eZ3SOxGfnEee31ie.QXwgDN1wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2) According to tee man page it can only duplicate data between files.
3) To duplicate data between commands we need to convert those commands to temporary files.
4) We need to duplicate the output of /challenge/hack as inputs of /challenge/the and /challenge/planet .
5) Enter /challenge/hack | tee >( /challenge/the ) >( /challenge/planet )

``` bash
Connected!
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >( /challenge/the ) >( /challenge/planet )
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
191432628719514542
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{cy-8f2HUX91eZ3SOxGfnEee31ie.QXwgDN1wCNyUzNzEzW}
hacker@piping~writing-to-multiple-programs:~
'''
6) Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i learned
1) How to duplicate the data between two commands by Process Substitution and tee command.
2) The tee command duplicates data between two files only.

## Split piping stderr and stdout
This challenge requires us to split the stderr and the stdout to two different commands using our knowledge.

**Flag**
pwn.college{cg48NpjjCBJ-c9k7n4GcA-fkMcw.QXxQDM2wCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i ./key hacker@dojo.pwn.college
```
2)We need to tranfer the stderr and stdout to their respective commands as inputs.
3) We need to use the pipe operator the stdout character and the stderr character.
4) Enter /challenge/hack | >( /challenge/planet ) 2>( /challenge/the )

``` bash
Connected!
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack | >( /challenge/planet ) 2>( /challenge/the )
bash: /dev/fd/63: Permission denied
Are you sure you're properly redirecting /challenge/hack's standard error into
'/challenge/the'?
You must redirect my standard error into '/challenge/the'!
Are you sure you're properly redirecting /challenge/hack's standard output into
'/challenge/planet'?
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{cg48NpjjCBJ-c9k7n4GcA-fkMcw.QXxQDM2wCNyUzNzEzW}
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack | > >( /challenge/planet ) 2> >( /challenge/the )
Are you sure you're properly redirecting /challenge/hack's standard error into
'/challenge/the'?
You must redirect my standard error into '/challenge/the'!
Are you sure you're properly redirecting /challenge/hack's standard output into
'/challenge/planet'?
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{cg48NpjjCBJ-c9k7n4GcA-fkMcw.QXxQDM2wCNyUzNzEzW}
hacker@piping~split-piping-stderr-and-stdout:~$
```
5) Copy and Paste the flag in the pwn.college website to complete the challenge.

##What i Learned
1)This challenge focus on the combining of the knowledge gained till now and use them to secure the required flag.
2) How to redirect the stderr and stdout to two different commands.

##Named Pipes
This challenge require us to make a FIFO file and redirect the output to it .

**Flag**
pwn.college{A_RinODoyOde2N9Q7MWGgJ8_r81.01MzMDOxwCNyUzNzEzW}

#Process
1) First  we need to connect the challenge to the terminal using
``` bash
ssh -i./key hacker@dojo.pwn.college
```
2)We need to make a FIFO named /tmp/flag_fifo .
3) Then we need to redirect the output of /challenge/run to the created FIFO.
4) The One problem with FIFOs is that they'll "block" any operations on them until both the read side of the pipe and the write side of 
the pipe are ready.
5) So we need to open another terminal.
6) In terminal 1 Enter mkfifo /tmp/flag_fifo
7) then after creatin Enter /challenge/run > /tmp/flag_fifo
8) In terminal 2 Enter cat /tmp/flag_fifo
9) After confirmation it will print out the flag.

``` bash
Terminal 1
Connected!
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!
Bash will now try to open the FIFO for writing, to pass it as the stdout of
/challenge/run. Recall that operations on FIFOs will *block* until both the
read side and the write side is open, so /challenge/run will not actually be
launched until you start reading from the FIFO!
hacker@piping~named-pipes:~$
```
``` bash
Terminal 2
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected/challenge/run's stdout to a FIFO at /tmp/flag_fifo! 
Here is your flag:
pwn.college{A_RinODoyOde2N9Q7MWGgJ8_r81.01MzMDOxwCNyUzNzEzW}
hacker@piping~named-pipes:~$
```
9) Copy and Paste the flag in the pwn.college website to complete the challenge.

#What i Learned
How to make a FIFO file using mkfifo command
Fifo file has both advantages and disadvantages 
No disk storage: FIFOs pass data directly between processes in memory - nothing is saved to disk

Ephemeral data: Once data is read from a FIFO, it's gone (unlike files where data persists)

Automatic synchronization: Writers block until the readers are ready, and vice-versa. It provides automatic synchronization. 

Complex data flows: FIFOs are useful for facilitating complex data flows, merging and splitting data in flexible ways, and so on.
For example, FIFOs support multiple readers and writers.






