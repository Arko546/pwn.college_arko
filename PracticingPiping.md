# Practicing Piping

## Redirecting output

Using the > function to put stdout to files.

### Solve
**Flag:** `pwn.college{I-bR5JGN_cVEmrQz-iWu2Y6LvaD.QX0YTN0wCNwAzNzEzW}`

I first got the output of PWN using echo and then redirected it to the COLLEGE file using '>' . 

```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{I-bR5JGN_cVEmrQz-iWu2Y6LvaD.QX0YTN0wCNwAzNzEzW}
```

### New learnings

I learnt how to use the '>' command to redirect stdout to files.

### References

*********

## Redirecting more output

Using the> function to redirect the stdout to files.

### Solve
**Flag** `pwn.college{kg9BOfnZA4zFF6fBB3ZBzLFsloO.QX1YTN0wCNwAzNzEzW}`

I used > funtion to redirect the output to myflag file. The i read the myflag file to get the file.

```bash
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{kg9BOfnZA4zFF6fBB3ZBzLFsloO.QX1YTN0wCNwAzNzEzW}
```
### New learnings

I learnt more about the use of > command.

### References
**********

## Appending output

### Solve
**Flag:** `pwn.college{0dGB9VVUOOoiRrm2jI9JM9sqTP_.QX3ATO0wCNwAzNzEzW}`

I appended the stdout of /challenge/run to the ~/the-flag. The ~/the-flag already had the first half of the flag. After appending the second half was also attached to it. This is how I got the flag.

```bash
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat ~/the-flag
 |
\|/ This is the first half:
 v
pwn.college{0dGB9VVUOOoiRrm2jI9JM9sqTP_.QX3ATO0wCNwAzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
```

### New learnings

I learnt how to append a stdout onto another file.

### Resources
***********

## Redirecting errors

Redirecting the errors and outputusing specific instructions.

### Solve
**Flag** `pwn.college{gRuswB5w-GfZQmrGXoh4XIUciZL.QX3YTN0wCNwAzNzEzW}`

I redirected the output of /challenge/run to myflag using 1> and the errors to intruction file using 2> . Then I used the cat command to read the myflag file that has the the flag.


```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{gRuswB5w-GfZQmrGXoh4XIUciZL.QX3YTN0wCNwAzNzEzW}
```

### New learnings
I learnt how to redirect the output, and errors individually.

### References

**********


## Redirecting Input

Using < to redirect input.

### Solve
**Flag:** `pwn.college{0uxAGuh9outmC4-ByXUTdENroCj.QXwcTN0wCNwAzNzEzW}`

First I used echo to get the value COLLEGE into the PWN file. I used < to redirect the input of PWN file to the /challenge/run directory and got the flag.

```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{0uxAGuh9outmC4-ByXUTdENroCj.QXwcTN0wCNwAzNzEzW}
```

### New learnings
I learnt how to redirect input.

### References
*************

## Grepping stored results

Using grep to search from stored results.

### Solve
**Flag:** `pwn.college{oDCnduay8s4iUT5jAp-pxvQWrKw.QX4EDO0wCNwAzNzEzW}`

I first redirected the output of the /challenge/run directory to the /tmp/data.txt using > . Then I used grep to search for the flag from the stored results in /tmp/data.txt file.

```bash
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
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{oDCnduay8s4iUT5jAp-pxvQWrKw.QX4EDO0wCNwAzNzEzW}
```
### New learnings

I learnt how to implemnt grep command to search in from the outputs stored using >. 

### References
**********

## Grepping live output

Using the pipe command to quickly search for desired output.

### Solve
**Flag:** `pwn.college{cHzIaHy5tmWcLD2tYzMd5uOFLLJ.QX5EDO0wCNwAzNzEzW}`

I first ran the output on the left side of the pipe and then searched for the flag on the right side of the flag using grep.

```bash
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
pwn.college{cHzIaHy5tmWcLD2tYzMd5uOFLLJ.QX5EDO0wCNwAzNzEzW}
```

### New learnings
I learnt how to use the pipe command.

### References
No refernces used.
***************

## Grepping errors

Redirecting stderr to stdout.

### Solve 
**Flag:** `pwn.college{4dX56rRIp54y3tFu9CjSeXLoPuo.QX1ATO0wCNwAzNzEzW}`

I redirected the stderr to stdout using 2 >& 1. Then I piped it to the grep command which searched for the flag.

```bash
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
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
```

### New learnings
I learnt how to redirect stderr to stdout.

### Refernces
************

## Filtering with grep -v

Using grep -v toh fileter out the values we dont want.

### Solve
**Flag:** `pwn.college{EXT6FbLRbuyC15yF5hpBnaYHCcl.0FOxEzNxwCNwAzNzEzW}`

First I got the output of the /challenge/run and piped it to grep -v with the argument of DECOY which will give us all the lines not conataing the word DECOY in it. And this is how I got the flag.

```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{EXT6FbLRbuyC15yF5hpBnaYHCcl.0FOxEzNxwCNwAzNzEzW}
```

### New learnings
I learnt how to use grep -v command.

### References 
**************

## Duplicating piped data with tee

Using the tee command to duplicate a piped data to any number of files and itercept it for debugging.

###  Solve
**Flag:** `

First I piped the output of the given directory to the other final directory and intercepted it with the tee command and stored the result in a file called output. Then I read the ouput file using cat which told me which argument to use after the initial directory. I then passed the resulting value to the final directory given using the pipe function.

```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee output1 | /challenge/college
Processing...
WARNING: you are overwriting file output1 with tee's output...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat output1
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "k5HY_ajD"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret k5H
Y_ajD | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{k5HY_ajDaT-pOiamVwKLmyXEyCK.QXxITO0wCNwAzNzEzW}
```

### New learnings
I learn how to intercept pipe using tee command and store it in a file for debugging. 

### References
**************

## Process substitution for input

Learning to use process substitution.

### Solve
**Flag:** `pwn.college{YR8B5EWLWA68lTgZsuiuLz_9orj.0lNwMDOxwCNwAzNzEzW}`

I used process substitution to create temp files for both the directories outputs and then wrote diff command before them to find the flag.

```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
27a28
> pwn.college{YR8B5EWLWA68lTgZsuiuLz_9orj.0lNwMDOxwCNwAzNzEzW}
```

### New learnings

I learned how to find difference between outputs of two directories using process substitution.

### References
**************

## Writing to multiple programs

Using the process substitution for multiple directories.

### Solve
**Flag:** `pwn.college{UGFYl2WaDUs1tUsKdKDIFF_xMGA.QXwgDN1wCNwAzNzEzW}`

I copied the output of the /challenge/hack command as input to the /challenge/the and /challenge/planet directories. This then used the output of the first part as input for the other two and gave me the flag.

```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
55161761940762289
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{UGFYl2WaDUs1tUsKdKDIFF_xMGA.QXwgDN1wCNwAzNzEzW}
```

### New learnings

I learnt how to use process substitution to subtitute and output of a command to various directories as input.

### References
No refernces used

## Split piping stderr and stdout

Redirecting the stderr and stdout into two diffferent programs using piping.

### Solve
**Flag:** `
I redirected the stderr to the /challenge/the command and stdout to the /challlenge/planet and connected them by pipe.

```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) | (/challenge/planet)
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{sljbCBaw4tuPPEYOj7ORgL1RWw8.QXxQDM2wCNwAzNzEzW}
```

### New learnings

I learnt how to redirect the stderr and stdout of a command to two seperate commands using piping.

### References
**********

## Named pipes

Making a named pipe and running a program through it.

### Solve
**Flag:** `pwn.college{Ebg4dl4f4g2hd0upSkVayiB099a.01MzMDOxwCNwAzNzEzW}`

First I made a FIFO file. Then I redirected the output to the FIFO file. This is the write part of the program. To run through the pipe it also needs the reading part. In a new terminal I will read the FIFO file. This will give me the flag in the other terminal.

Terminal 1
```bash








