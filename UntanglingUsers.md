# UNTANGLING USERS

## Becoming root with su
Ho wot become root user with su command.

### Solve
**Flag:**`pwn.college{k9yxpogWvmBY6YRY4RHsGqWqeP2.QX1UDN1wCNwAzNzEzW}`

I used the su command to enter the password and become root.

```bash
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{k9yxpogWvmBY6YRY4RHsGqWqeP2.QX1UDN1wCNwAzNzEzW}
root@users~becoming-root-with-su:/home/hacker#

```

### New learnings
Learning how to become root using su.

### References
********************

## Other users with su
Becoming other user with su command.

### Solve
**Flag:**`pwn.college{QlZyjq3YTMtDFWjcXGTETisvuar.QX2UDN1wCNwAzNzEzW}`

I used the su command followed by zardus to become zardus user.

```bash
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{QlZyjq3YTMtDFWjcXGTETisvuar.QX2UDN1wCNwAzNzEzW}
```

### New learnings
I learnt how to become other user using su.

### Refernces
*******************

## Using sudo

Using sudo to gain access to give adminitration pemission.

### Solve 
**Flag:**`pwn.college{4QUNI9pt7BA92UFvJM7oSrxjxto.QX4UDN1wCNwAzNzEzW}`

I used the sudo command followed by cat /flag to read it.

```bash
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{4QUNI9pt7BA92UFvJM7oSrxjxto.QX4UDN1wCNwAzNzEzW}
```

### new learnings
I learnt how to use sudo command

### References
*********************
