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


##


