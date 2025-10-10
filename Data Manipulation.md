## Data Manipulation
This is the eight module in the Linux Luminarium.
This module contains Six challenges .
1)Translating Characters .
2)Deleting Characters .
3) Deleting New Lines .
4) Extracting the first lines with head .
5)  Extracting specific section of the text .
6) Sorting Data .

##Translating Characters
This challenge requires us to translate the character provided in its first argument to the character provided in its second argument.

**Flag**
pwn.college{giA29uTZJMllbyy-61QS-cjDuIv.01MxEzNxwCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)We need to  translate the character provided in its first argument to the character provided in its second argument.
3)For this to satisfy we need to use the tr command.
4) We need to translate every lowercase letters with upper case letters and vice versa.
5)Enter cat /challenge/run | tr '[a-Z][A-z]' '[A-z][a-Z]'

 ``` bash
Connected!
hacker@data~translating-characters:~$ cat /challenge/run | tr Aa aA
#!/opt/pwn.college/bAsh
echo "Your cAse-swApped flAg:"
cAt /flAg | tr '[a-Z][A-z]' '[A-z][a-Z]'
echo
hacker@data~translating-characters:~$ cat /challenge/run | tr '[a-Z][A-z]' '[A-z][a-Z]'
tr: range-endpoints of 'a-Z' are in reverse collating sequence order
hacker@data~translating-characters:~$ /challenge/run | tr 'a-zA-Z' 'A-Za-z'
yOUR CASE-SWAPPED FLAG:
pwn.college{giA29uTZJMllbyy-61QS-cjDuIv.01MxEzNxwCNyUzNzEzW}
```
6)Copy and Paste the flag in the pwn.college website to complete the challenge .

#What i Learned
1) How to translate the characters which we dont want with wich we want .
2)For this we need touse tr command .

##Deleting Characters
This challenge requires us to translate the characters to nothing .

**Flag**
pwn.college{UjckXG5g4fjuivlTUAzAdk5ELTu.0FNxEzNxwCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)Unlike the above challenge , in this challenge we need to translate the charactes to nothing .
3)For this to occur we need to use tr -d command instead of tr command .
4)This will translate the characters which we dont want to nothing .
5)In this challenge the flag we need aslo contains the characters which we do not need .
6)Enter /challenge/run | tr -d '^%'

``` bash
Connected!
hacker@data~deleting-characters:~$ cat /challenge/run | tr -d '^%'
#!/opt/pwn.college/bash

echo "Your character-stuffed flag:"
cat /flag | while IFS= read -n1 c; do
  printf 's' "$c"
  (( RANDOM  100 < 60 )) && printf ''
  (( RANDOM  100 < 60 )) && printf ''
done
echo
hacker@data~deleting-characters:~$ /challenge/run | tr -d '^%'
Your character-stuffed flag:
pwn.college{UjckXG5g4fjuivlTUAzAdk5ELTu.0FNxEzNxwCNyUzNzEzW}
hacker@data~deleting-characters:~$
```
7)Copy and Paste the flag in the pwn.college website to complete the challenge .

#What i learned
1)I learned how to remove unwanted characters present in the output .
2)For this we need to use tr -d command.

##Deleting New Lines
In this challenge we need to delete new lines to get the require flag .

**Flag**
pwn.college{c4jSTxSVMoj2AgdHJzIkdeaFkNg.0VNxEzNxwCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)Newlines refers to a special character that indicates the end of a line of text and the beginning of a new one. 
3) To delete new lines we need to use a escape sequence \n  in quotes .
4)Since we want to delete them we need to use tr -d command
5)Enter /challenge/run | tr -d '\n' .  

``` bash
Connected!
hacker@data~deleting-newlines:~$ /challenge/run | tr -d '\n'
Your line-split flag: pwn.college{c4jSTxSVMoj2AgdHJzIkdeaFkNg.0VNxEzNxwCNyUzNzEzW}hacker@data~deleting-newlines:~$
```
6)Copy and Paste the flag in the pwn.college website to complete the challenge .

#What i Learned 
1)How to delete new lines and what are those .
2)We need to use /n escape sequence to delete these newlines.

##Extracting the first lines with head
This challenge requires us to extract the required lines from the output .

**Flag**
pwn.college{8eXbl5lyH0RY39No-VZu16rhUN8.0lNxEzNxwCNyUzNzEzW}

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)We need to get only the required lines in the output.
3)For this we use the head command .
4)By default, it shows the first 10 lines.
5)But to get less or more than 10lines we need to use  -n option.
6)In this challenge we need to extract the first seven lines of the output .
7)But we need to pipe the data to the head command .
8)Enter cat /challenge/.codes | head -n 7 | /challenge/college

``` bash 
Connected!
hacker@data~extracting-the-first-lines-with-head:~$ echo /challenge/pwn | head -n 7 | /challenge/college
Invalid codes!
hacker@data~extracting-the-first-lines-with-head:~$ cat /challenge/.codes
SECRET-CODE-24653
SECRET-CODE-3545
SECRET-CODE-9349
SECRET-CODE-20814
SECRET-CODE-32366
SECRET-CODE-2715
SECRET-CODE-26938
SECRET-CODE-4555
SECRET-CODE-10236
SECRET-CODE-18707
SECRET-CODE-1298
SECRET-CODE-31748
SECRET-CODE-31317
SECRET-CODE-30267
SECRET-CODE-18935
SECRET-CODE-846
SECRET-CODE-31788
SECRET-CODE-11910
SECRET-CODE-4086
SECRET-CODE-26680
hacker@data~extracting-the-first-lines-with-head:~$ cat /challenge/.codes | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{8eXbl5lyH0RY39No-VZu16rhUN8.0lNxEzNxwCNyUzNzEzW}
hacker@data~extracting-the-first-lines-with-head:~$
```
9)Copy and Paste the flag in the pwn.college website to complete the challenge .

#What i Learned
1)How to extract only the required number of lines from the output.
2)We need to use head command for this .

## Extracting specific section of the text 
Unline the above challenge this challenge require us to extract required columns from the output.

**Flag
pwn.college{wPBrI_YcEmmfNSNDSKQ770Jenzw.01NxEzNxwCNyUzNzEzW

#Process
1)First we need to connect the challenge to the terminal using
''' bash
ssh -i ./key hacker@dojo.pwn.college
'''
2)Unlike the above challenge in here we need to extract required columns from the output.
3)We need to use cut to extract specific columns along with -d argument which specifies the column delimiter .
4)Example  cut -d " " -f 1 scores.txt 
             gives the first column of the output.
5)This challenge,gives a program will give you a bunch of lines with random numbers and single characters (characters of the flag) as columns.
6)Then then we need topipe it to the  tr -d "\n" .
7)Enter  /challenge/run | cut -d ' ' -f 2 | tr -d '\n'

``` bash
Connected!
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run cut -d " " -f 2
10841 p
22576 w
21007 n
2347 .
30921 c
5560 o
31964 l
4032 l
7769 e
6769 g
4816 e
14066 {
28699 w
11679 P
12559 B
31614 r
11162 I
14133 _
1418 Y
21036 c
22711 E
1595 m
6946 m
27156 f
30295 N
26073 S
15205 N
30628 D
23335 S
1776 K
6869 Q
21984 7
501 7
2092 0
5527 J
29323 e
13044 n
22640 z
14310 w
624 .
15918 0
22364 1
26448 N
22853 x
32666 E
30020 z
26411 N
17708 x
32157 w
23656 C
18665 N
30695 y
31986 U
3980 z
13838 N
3980 z
20841 E
24929 z
14396 W
6639 }
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d ' ' -f 2 | tr -d '\n'
pwn.college{wPBrI_YcEmmfNSNDSKQ770Jenzw.01NxEzNxwCNyUzNzEzW}hacker@data~extracting-specific-sections-of-text:~$
```
8)Copy and Paste the flag in the pwn.college website to complete the challenge .

#What i Learned
1)How to extract only the required columns from the total output .
2)For this we need to use cut command and use -d for specifing the column and column number which we want to extract .






