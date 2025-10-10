# Perceiving Permissions

## Changing file ownership

Using the chown command to change ownership of flag.

### Solve
**Flag:**``

First I changed the ownership of the flag using the chown to the user hacker. Then I read the file using cat.

```bash
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{ExXwO21MF-2MSuQNkPLWhU4rC6N.QXxEjN0wCNwAzNzEzW}
```

### New learnings

I learnt how to use the chown command to change the ownership of a file to a different user.

### References
********************


## Groups and files

Gving access of files to groups.

### Solve
**Flag:**`pwn.college{QSSlw9znb39pSCt_jjXPGABzuIz.QXxcjM1wCNwAzNzEzW}`

I used the chgrp command to make the file a readable to the group. Then got the flag using cat.

```bash
hacker@permissions~groups-and-files:~$ ls -l
total 32
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
hacker@permissions~groups-and-files:~$ chgrp hacker not-the-flag
hacker@permissions~groups-and-files:~$ cat not-the-flag
pwn.college{QSSlw9znb39pSCt_jjXPGABzuIz.QXxcjM1wCNwAzNzEzW}
```

### New learnings

I learnt how to change membership of a file to a group.

### References
****************

## Fun with group names

Changing the group of a file to soe other user's group.

### Solve
**Flag:**`pwn.college{wa41mJlmSwH8HoHrV1cZWdUj9y9.QXycjM1wCNwAzNzEzW}`

I first got the grp id using id. Then changed the grp of to the new grp id. And the finally read the flag.

```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp29073) groups=1000(grp29073)
hacker@permissions~fun-with-groups-names:~$ chgrp grp29073 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{wa41mJlmSwH8HoHrV1cZWdUj9y9.QXycjM1wCNwAzNzEzW}
```

### New learnings

I learnt how to change the ownership to some other grp except the orignal user.

### Refernces
************

## Chnaging permissions

I learnt how to change permission using chmod.

### Solve
**Flag:**`pwn.college{wlaGXaOGfUAp8BYmWKVCWBGUxpY.QXzcjM1wCNwAzNzEzW}`

First I used the chmod with o+r which basically gives other users the permission to read the /flag file.

```bash
hacker@permissions~changing-permissions:~$ chmod o+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{wlaGXaOGfUAp8BYmWKVCWBGUxpY.QXzcjM1wCNwAzNzEzW}
```

### New learnings

I learnt how to use the chmod to give permission to other users.

### References
Chatgpt
******************

## Executable files

Making file executable using by giving persmission using chmod.

### Solve
**Flag:**`pwn.college{MS69Yrn8Evy7LWcp9B8L2YOMcPV.QXyEjN0wCNwAzNzEzW}`

I used u+x to give the user the permission to read the execute /challenge/run.

```bash
Connected!
hacker@permissions~executable-files:~$ chmod o-x /challenge/run
hacker@permissions~executable-files:~$ ls -l /challenge/run
-r--r--r-- 1 hacker hacker 32 Jan 14  2025 /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
bash: /challenge/run: Permission denied
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{MS69Yrn8Evy7LWcp9B8L2YOMcPV.QXyEjN0wCNwAzNzEzW}
```

### New learnings

I learnt about chmod u+x which gives permission to the user to execute files or programs.

### Refereces 
Chatgpt
*****************

## Permission tweaking practice


