# Shell Variables

## Printing variables

Learn how to print variables.

### Solve
**Flag:**`pwn.college{EfLBULupnxPotOJ8-Jxv5ud_FBD.QX3UTN0wCNwAzNzEzW}`

Print the random variable using the $ function.

```bash
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{EfLBULupnxPotOJ8-Jxv5ud_FBD.QX3UTN0wCNwAzNzEzW}
```

### New learnings

I learnt how to print variables.

### References
***********

## Setting Variable

Learn how to set value for vairable.

### Solve
**Flag:**`pwn.college{MqKI8PbYAFPJNc6cNDvG8wcsDN8.QX5UTN0wCNwAzNzEzW}`

Used the = sign to set the value of PWN variable.

```bash
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{MqKI8PbYAFPJNc6cNDvG8wcsDN8.QX5UTN0wCNwAzNzEzW}
```

### New learnings
I learnt how to set value for a variable

### References
***************

## Multi-word variables

Learning how to assign multiples words to a variable.

### Solve
**Flag:**`pwn.college{k_aH_GSYTkRHxfm7ctUtPzJhZcT.QXwYTN0wCNwAzNzEzW}`

Using the " " to put multiple words in a variable.

```bash
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{k_aH_GSYTkRHxfm7ctUtPzJhZcT.QXwYTN0wCNwAzNzEzW}
```
### New learnings
I learnt how to use "" to put multiple words in a variable.

### References
***********

## Exporting Variables

Learning how to export data in shell variables.

### Solve
**Flag:**`pwn.college{EmJqGhbANpgudljNI9buVLLVnQ6.QXyYTN0wCNwAzNzEzW}`

Exporting the PWN variable with COLLEGE value. Running PWN to get the flag.

```bash
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run PWN
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{EmJqGhbANpgudljNI9buVLLVnQ6.QXyYTN0wCNwAzNzEzW}
You've set the PWN variable to the proper value!
```

### New learnings

Learnt how to export values from variable.

### References
*********

## Printing exported variables
Using the env command to show list of variables

### Solve
**Flag:** `pwn.college{cEfyM6QYKSyvyc_W9P7bA13NFsI.QX4UTN0wCNwAzNzEzW}`

Using env to get list of variables and the printing the FLAG variable to get flag.
```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=a2e36b5934c926d9cd8d1ab08e98b0a07484579ed30c96bdf23af356fe7c3d41
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{cEfyM6QYKSyvyc_W9P7bA13NFsI.QX4UTN0wCNwAzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
hacker@variables~printing-exported-variables:~$ env $FLAG
env: ‘pwn.college{cEfyM6QYKSyvyc_W9P7bA13NFsI.QX4UTN0wCNwAzNzEzW}’: Permission denied
```

### New learnings
I learnt how to list variables.

### References
***************

## Storing command output

Storing command outputs into variables.

### Solve
**Flag:** `pwn.college{Qh2NbG9y-KX6WkC0D3F2ha5QteN.QX1cDN1wCNwAzNzEzW}`

Storing the value of of command into a variable.

```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo "$PWN"
pwn.college{Qh2NbG9y-KX6WkC0D3F2ha5QteN.QX1cDN1wCNwAzNzEzW}
```

### New leanings

I learnt how to store command output into variables.

### References
***********

## Reading Input

Using read command to set input in a variable.

### Solve
**Flag:** `pwn.college{M1KdB9PsNU-0pvj7kOiaCBEI-FZ.QX4cTN0wCNwAzNzEzW}`

I used read and the variable PWN to enter a value for the variable. Then I entered the value COLLEGE.

```bash
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{M1KdB9PsNU-0pvj7kOiaCBEI-FZ.QX4cTN0wCNwAzNzEzW}
```

### New learnings

I learnt how to input a value for a variable using read.

### References
****************

## Reading files

Using the read function to input files as input to variables.

### Solve
**Flag**`pwn.college{UeuMgRGmOuVjViBg7mrBW3MM0LV.QXwIDO0wCNwAzNzEzW}`

I redirected the output of /cahallenge/read_me as input to the PWN variable and read it.

```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{UeuMgRGmOuVjViBg7mrBW3MM0LV.QXwIDO0wCNwAzNzEzW}
```

### New learnings

I learnt how to redirect a file as an input and read it.

### References
No references used.
***************
