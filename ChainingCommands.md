# Chaining Commands

## Chaining with semicolons

Using semi colons to chain commands.

### Solve
**Flag:** `pwn.college{oJ-ZjpG6tQW17lWSc_mbW1KC8ct.QX1UDO0wCNwAzNzEzW}`

Using the semicolon to chain the two directories together.

```bash
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{oJ-ZjpG6tQW17lWSc_mbW1KC8ct.QX1UDO0wCNwAzNzEzW}
```

### New learnings
I learnt how to chain commands using semi colon.

### References
************

## Building on success

Using && to link two commands

###  Solve
**Flag:**`pwn.college{kwTtZ0r_FWag8_hcA_NDqgD3rIs.0lM0MDOxwCNwAzNzEzW}`

I used && to link th two commands.

```bash
hacker@chaining~building-on-success:~$ /challenge/first-success && /challeng
e/second
Nice chaining! Flag: pwn.college{kwTtZ0r_FWag8_hcA_NDqgD3rIs.0lM0MDOxwCNwAzNzEzW}
```
### New learnings
I learnt how to link two commands using &&.

### Referenes
***************

## Building on success

Using || to choose between two commands

###  Solve
**Flag:**`pwn.college{YqSNJCWLAl5RJQrvTt9hHfuivwd.01M0MDOxwCNwAzNzEzW}`

I used && to link th two commands.

```bash
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/s
econd
Nice chaining! Flag: pwn.college{YqSNJCWLAl5RJQrvTt9hHfuivwd.01M0MDOxwCNwAzNzEzW}
```
### New learnings
I learnt how to link two commands using ||.

### Referenes
***************


## Your first shell script

Making a shell script.

### Solve
**Flag:**``

Echoed the output of the two commands into x.sh

```bash
hacker@chaining~your-first-shell-script:~$ echo -e "/challenge/pwn ; /challe
nge/college" > x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{ECjO9aqkyxo3DGuZ6_zLkyj0TGB.QXxcDO0wCNwAzNzEzW}
```

### New learnings
I learnt how to create a shell script.

### Refernces
**************

## Redirecting script output

Redirectin output of a shell script.

### Solve
**Flag:**``

Echoed the output of the two commands into x.sh and then piped the output into /challenge/solve

```bash
hacker@chaining~redirecting-script-output:~$ echo -e "/challenge/pwn ; /challenge/college" > x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{gmWRVwhsFm1D8ZFf5MyNAlmf0FO.QX4ETO0wCNwAzNzEzW}
```

### New learnings
I learnt how to create a shell script.

### Refernces
**************

## Executable shell scripts

### Solve
**Flag:** `

I echoes the output into the shell scrpt. Then gave the permission to execute and read to the the user, group and others.

```bash
hacker@chaining~executable-shell-scripts:~$ echo -e "/challenge/solve" > x.s
h
hacker@chaining~executable-shell-scripts:~$ ls -l
total 36
-rw-r--r-- 1 hacker hacker   4 Sep 28 09:12 COLLEGE
-rw-r--r-- 1 hacker hacker   8 Sep 28 09:51 PWN
-rw-r--r-- 1 root   hacker  60 Sep 26 12:52 a
-rw-r--r-- 1 hacker hacker   0 Oct 10 04:19 college_file
-rw-r--r-- 1 hacker hacker   0 Sep 27 22:20 foo.1x.dvi
-rw-r--r-- 1 hacker hacker 829 Sep 28 09:40 instructions
-rw-r--r-- 1 hacker hacker  95 Sep 28 09:40 myflag
lrwxrwxrwx 1 hacker hacker   5 Sep 27 09:29 not-the-flag -> /flag
-rw-r--r-- 1 root   hacker  77 Sep 28 11:05 output1
drwxr-xr-x 1 hacker hacker   0 Oct 10 04:18 pwn_directory
-rw-r--r-- 1 hacker hacker 437 Sep 28 09:30 the-flag
-rw-r--r-- 1 hacker hacker  17 Oct 11 12:11 x.sh
hacker@chaining~executable-shell-scripts:~$ chmod u=xr, g=xr, o=xr x.sh
chmod: invalid mode: ‘u=xr,’
Try 'chmod --help' for more information.
hacker@chaining~executable-shell-scripts:~$ chmod u=xr,g=xr,o=xr x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
Congratulations on your shell script execution! Your flag:
pwn.college{kjJOZjw3Rm_wDFgGfOMr3s5Dc1v.QX0cjM1wCNwAzNzEzW}
```

### New learnings
I learnt shell script is excutable. I caninvoke it without having to bash it.

### Referncces
******************


