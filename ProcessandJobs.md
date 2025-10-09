# Process and Job

## Listing processes
Using varous commands to list processes

### Solve
**Flag:**`pwn.college{QnzsXCdPC3xHK3DFX0iRold11Q6.QX4MDO0wCNwAzNzEzW}`

```bash
hacker@processes~listing-processes:~$ ps -efww | grep '/challenge/'
root         132       1  0 21:05 ?        00:00:00 /challenge/9973-run-22891
hacker       153     143  0 21:06 pts/0    00:00:00 grep --color=auto /challenge/

hacker@processes~listing-processes:~$ /challenge/9973-run-22891
Yahaha, you found me! Here is your flag:
pwn.college{QnzsXCdPC3xHK3DFX0iRold11Q6.QX4MDO0wCNwAzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```

## New learnings
I learnt how to use list.

**********

## Killing processes

Using sleep to sleep programs.

### Solve
**Flag:**`pwn.college{w274_P-eFg0MG20UeirazhH3Vt8.QXyQDO0wCNwAzNzEzW}`

I used the sleep command to sleep the other progra and run the new one instead.

```bash
hacker@processes~killing-processes:~$ ps -e | grep sleep
    137 ?        00:00:00 sleep
    156 pts/0    00:00:00 sleep

hacker@processes~killing-processes:~$ kill 137
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{w274_P-eFg0MG20UeirazhH3Vt8.QXyQDO0wCNwAzNzEzW}
```

## New learnings
I learnt how to use sleep oommand.
***************

## Interrupting processes

Using ctrl c to interrupt a command running.

### Solve
**Flag:**`pwn.college{QGwk8ozbiUKRCggMG21gbColSe0.QXzQDO0wCNwAzNzEzW}`

I used the ctrl c to interrupt the command /challenge/run and got the flag.

```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{QGwk8ozbiUKRCggMG21gbColSe0.QXzQDO0wCNwAzNzEzW}
```

## New learnings

I learnt how to intterupt a running command.
*****************

## Suspending process

Using ctrl z to suspend processes.

### Solve
**Flag:**`pwn.college{oao_lFRcqmkiPr3o2MuObqOUZYo.QX1QDO0wCNwAzNzEzW}`

I used the the ctrl z to suspend the command and then ran another copy of the same command.

```bash
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         162     152  0 17:59 pts/1    00:00:00 bash /challenge/run
root         164     162  0 17:59 pts/1    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         162     152  0 17:59 pts/1    00:00:00 bash /challenge/run
root         169     152  0 17:59 pts/1    00:00:00 bash /challenge/run
root         171     169  0 17:59 pts/1    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{oao_lFRcqmkiPr3o2MuObqOUZYo.QX1QDO0wCNwAzNzEzW}
```

### New learnings

I learnt how to suspend a command.
**************

## Resuming processes

Learning how to resume commands.

### Solve
**Flag**`pwn.college{A3b4pLcq55sFM1ZBxBxbjS_1Ply.QX2QDO0wCNwAzNzEzW}`

I first paused the program and then resumed it with fg.

```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
z^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{A3b4pLcq55sFM1ZBxBxbjS_1Ply.QX2QDO0wCNwAzNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

### New learning
I learnt how to use the fg command to resume a program.
******************

## Background processes

Using the bg command to move program to background

### Solve
**Flag:**`pwn.college{U2ud4SOOeqc6IhBNpz3QgwOru6G.QX3QDO0wCNwAzNzEzW}`

I first put the command in the background then ran another copy which gave me the flag.

```bash
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         139 S+   bash /challenge/run
root         141 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         139 S    bash /challenge/run
root         149 S    sleep 6h
root         150 S+   bash /challenge/run
root         152 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{U2ud4SOOeqc6IhBNpz3QgwOru6G.QX3QDO0wCNwAzNzEzW}
```

### New learnings
I learnt how to move proceses into the background

**********

## Foregrounding processes

Putting processes int he foreground.

### Solve
**Flag:** `pwn.college{Qi0gNP46w1aDFqKQEtO-DtO0ssj.QX4QDO0wCNwAzNzEzW}`

I suspended the program and sen it to the background. Then used the fg command to send it to foreground.

```bash
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.

hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{Qi0gNP46w1aDFqKQEtO-DtO0ssj.QX4QDO0wCNwAzNzEzW}
```

### New learnings
I learnt how to put programs in the foreground

*****************

##  Starting background processes

Running processes directly from background

### Solve
**Flag:**``

I used the & command to specifically start the program from background.

```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run & [1] 1771
[1] 138
bash: [1]: command not found
hacker@processes~starting-backgrounded-processes:~$


Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{cLimDgi9Z9yYqIrwMHcc4ORCdMk.QX5QDO0wCNwAzNzEzW}

[1]+  Done                    /challenge/run
```

### New learnings
I learnt how start a program from background.
*************




