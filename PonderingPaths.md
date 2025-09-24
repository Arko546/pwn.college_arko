# Pondering Paths

## The Root

Invoking a program using by providing its path using "/"

### Solve

**Flag:** `pwn.college{ImYc3BUkssFR9jVY0I3JBbuEU0Z.QX4cTO0wCNwAzNzEzW}`

Using / allows me to access different paths for different programs. In this case we will be using /pwn to directly access the pwn program and run it.

```bash
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{ImYc3BUkssFR9jVY0I3JBbuEU0Z.QX4cTO0wCNwAzNzEzW}
```

### New learnings 

This challenge helped me to learn how to access different programs under / and also taught me how to directly access a program.

### References

No reference used


## Programs and Absolute Paths

Accessing a program that is under a directory that is under the / directory

### Solve

**Flag:** `pwn.college{kiJ8h_GKiYV3EKso8olRW6JlF10.QX1QTN0wCNwAzNzEzW}`

To access the run file I first need to access the challenge directory that is under the / directory. So my command basically goes to the challenge directory and the to the run 

```bash
file.Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{kiJ8h_GKiYV3EKso8olRW6JlF10.QX1QTN0wCNwAzNzEzW}
```

### New learnings

In this challenge we learnt how to access files that are under a directory that is under / using absolute path.

### References 

No references used


## Position thy self

Accessing a program from a specific directory 

### Solve 
**Flag** `pwn.college{Ems9GoOuwMn8MU8SZDYPljOoqMb.QX2QTN0wCNwAzNzEzW}`

First i needed to find from the i needed to run the directory. I got that by using the command given. Then I used cd to change to the given directory. After that i used absolute path from that directory to get the flag.

```bash
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /sys directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /sys
hacker@paths~position-thy-self:/sys$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Ems9GoOuwMn8MU8SZDYPljOoqMb.QX2QTN0wCNwAzNzEzW}
```

### New Learnings

I learnt how to change directories using the cd command.

### References

No references used.


## Position elsewhere

Changing directories using cd

### Solve 
**Flag** `pwn.college{A9nQBLje58mzU7NIRUFu9a_M010.QX3QTN0wCNwAzNzEzW}`

First i needed to find from the i needed to run the directory. I got that by using the command given. Then I used cd to change to the given directory. After that i used absolute path from that directory to get the flag.

```bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /var directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /var
hacker@paths~position-elsewhere:/var$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{A9nQBLje58mzU7NIRUFu9a_M010.QX3QTN0wCNwAzNzEzW}
```

### New Learnings

I learnt how to change directories using the cd command and accessing directories from there.

### References

No references used.


## Positon yet elsewhere

Changing directories using cd

### Solve 
**Flag** `pwn.college{A9nQBLje58mzU7NIRUFu9a_M010.QX3QTN0wCNwAzNzEzW}`

First i needed to find from the i needed to run the directory. I got that by using the command given. Then I used cd to change to the given directory. After that i used absolute path from that directory to get the flag.

```bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /var directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /var
hacker@paths~position-elsewhere:/var$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{A9nQBLje58mzU7NIRUFu9a_M010.QX3QTN0wCNwAzNzEzW}
```

### New Learnings

I learnt how to change directories using the cd command and accessing directories from there.

### References

No references used.

## implicit relative paths, from /

Accessing files from a relative path.

### Solve 
**Flag** `pwn.college{Ilgh9b_LlNjbMVQ18z7I7ZXbgx0.QX5QTN0wCNwAzNzEzW}`

To execute a file from a relative path, i need to first to the specific directory which is / in this case. Next I ran a an absolute path relative to the / directory which found the flag.

```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{Ilgh9b_LlNjbMVQ18z7I7ZXbgx0.QX5QTN0wCNwAzNzEzW}
```

### New Learnings

I learnt about relative paths and how to execute them. I also learnt about current working directory. The cwd is the directory that the prompt is currently located at.

### References

No references used.




