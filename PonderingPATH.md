# Pondering PATH

## The path variable

Messing up the command by keeping black variable.

### Solve
**Flag**``

I kept the variabe blank so the rm command didnt work as intended and thus the flag was printed.

```bash
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{g_w7-m8UMHIyOvRT_9__pbkhAQS.QX2cDM1wCNwAzNzEzW}
```

### New learnings
I learnt that keeping the variable blank to mess up the command which is rm in this case.

### References
************************


## Setting path

Storing a list of directories in a variable.

### Solve
**Flag**``

I stored the list of directories in the PATH variable.

```bash
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{Imqwlv4fcthNk3pLFAP5GDIEmtj.QX1cjM1wCNwAzNzEzW}
```

### New learnings
I learnt how to store list of directories in variable.

### Refernces
************
## Finding commands

Using which to look through directories.

### Solve
**Flag:** `pwn.college{MXkOX1jQkFmG2DXkh-A95e8B2pK.01NzEzNxwCNwAzNzEzW}`

I used the which command to find in which directory win is. Then I read the flag as it is in the same directory as win.

```bash
hacker@path~finding-commands:~$ which win
/challenge/paths/19402/win
hacker@path~finding-commands:~$ cat /challenge/paths/19402/flag
pwn.college{MXkOX1jQkFmG2DXkh-A95e8B2pK.01NzEzNxwCNwAzNzEzW}
```

## New learnings
I leant how to use which.

### Referneces
********


