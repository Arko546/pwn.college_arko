# Terminal Multiplexing

## Launching Screen

Using screen command

### Solve
**Flag:**`pwn.college{Q0a9JdF9-an8aV5_UKfSBpbcUkF.0VN4IDOxwCNwAzNzEzW}`

I used the screen command to open screen.

```bash

Congratulations! You're inside a screen session!
Here's your flag:
pwn.college{Q0a9JdF9-an8aV5_UKfSBpbcUkF.0VN4IDOxwCNwAzNzEzW}
hacker@terminal-multiplexing~launching-screen:~$
```

### New learnings
I learnt how to open screen

### References
********************


## Detaching and attaching

Learning how to detach and rettach

### Solve
**FLag:**`pwn.college{YhddRc5kjb3fj0SOZK4Zytk1ZPM.0lN4IDOxwCNwAzNzEzW}`

I used the ctrl a and then d to detach after opeing screen then used screen -r to rettach.

```bash
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{YhddRc5kjb3fj0SOZK4Zytk1ZPM.0lN4IDOxwCNwAzNzEzW}
Yes! Flag is: pwn.college{YhddRc5kjb3fj0SOZK4Zytk1ZPM.0lN4IDOxwCNwAzNzEzW}
```

### New learnings
I leart how to rettach and detach.

### References
***************

## Finding sessions
Going through different screens to find the flag.

### Solve
**Flag:**`pwn.college{EKV9BH2oZ4TPA-DG1iDC4IRFow2.01N4IDOxwCNwAzNzEzW}`

I used screen -l to look through all the detach screen.

```bash

hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{EKV9BH2oZ4TPA-DG1iDC4IRFow2.01N4IDOxwCNwAzNzEzW}
pwn.college{EKV9BH2oZ4TPA-DG1iDC4IRFow2.01N4IDOxwCNwAzNzEzW}
hacker@terminal-multiplexing~finding-sessions:~$
```

### New learnings
I learnt how to look through various screens using screen -ls
### References
***************

## Switching windows

Learning to switch to different windows in the screen

### Solve
**Flag**` pwn.college{4sfsdH8z8txQZ3eYpYFQ9Uqn4VG.0FO4IDOxwCNwAzNzEzW}`

I opened the screena dn then went to the next window where the flag was hidden.

``` bash
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{4sfsdH8z8txQZ3eYpYFQ9Uqn4VG.0FO4IDOxwCNwAzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{4sfsdH8z8txQZ3eYpYFQ9Uqn4VG.0FO4IDOxwCNwAzNzEzW}
```

### New learning
I learnt how to look throuigh various screens.


*********

## Detaching and attaching tmux
Using tmux

### Solve
**Flag**` pwn.college{ADbzJr8qN_QqaFO458cUGCJnFTv.0VO4IDOxwCNwAzNzEzW}`

I launched tmux and the detached and rettached from it to get the flag.

```bash
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{ADbzJr8qN_QqaFO458cUGCJnFTv.0VO4IDOxwCNwAzNzEzW}
Congratulations, here is your flag: pwn.college{ADbzJr8qN_QqaFO458cUGCJnFTv.0VO4IDOxwCNwAzNzEzW}
```
### New learnings
I learnt about tmux.

### Refrences
*********

## Switching Windows

Learning how to switch beteeen windows in tmux

### Solve
**Flag:**` pwn.college{QUIMdpsF3xDzw7K3IHSIl-93LUJ.0FM5IDOxwCNwAzNzEzW}`

I opened tmux and then used the window picker to search through the windows to get the flag.

```bash
> Excellent work! You found window 0!
> Here is your flag: pwn.college{QUIMdpsF3xDzw7K3IHSIl-93LUJ.0FM5IDOxwCNwAzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{QUIMdpsF3xDzw7K3IHSIl-93LUJ.0FM5IDOxwCNwAzNzEzW}
hacker@terminal-multiplexing~switching-windows-tmux:~$
```

### New learnings
I learnt how to use the window picker command to switch through windows in tmux

### References
********************



