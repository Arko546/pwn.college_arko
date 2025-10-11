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
Using chmod to get a flag.

### Solve
**Flag:** `pwn.college{sZRNeqDpEF1v4KSdyGhqtPj1nn1.QXwEjN0wCNwAzNzEzW}`
I ran the challenge and and used chmod followed by the number.

```bash
hacker@permissions~permission-tweaking-practice:~$ /challenge/run
Round 1 of 8!

Current permissions of "/challenge/pwn": rw-r--r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": ---r--r--
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 044 /challenge/pwn
You set the correct permissions!
Round 2 of 8!

Current permissions of "/challenge/pwn": ---r--r--
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": -w-rw-r--
- the user doesn't have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 264 /challenge/pwn
You set the correct permissions!
Round 3 of 8!

Current permissions of "/challenge/pwn": -w-rw-r--
- the user doesn't have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": -wxrwxr--
- the user doesn't have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 374 /challenge/pwn
You set the correct permissions!
Round 4 of 8!

Current permissions of "/challenge/pwn": -wxrwxr--
- the user doesn't have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": -wxrwxr-x
- the user doesn't have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 375 /challenge/pwn
You set the correct permissions!
Round 5 of 8!

Current permissions of "/challenge/pwn": -wxrwxr-x
- the user doesn't have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": --xrwx--x
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 171 /challenge/pwn
You set the correct permissions!
Round 6 of 8!

Current permissions of "/challenge/pwn": --xrwx--x
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": -wxrwx-wx
- the user doesn't have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
* the world does have execute permissions
debug2: channel 0: window 999408 sent adjust 49168
hacker@permissions~permission-tweaking-practice:~$ chmod 373 /challenge/pwn
You set the correct permissions!
Round 7 of 8!

Current permissions of "/challenge/pwn": -wxrwx-wx
- the user doesn't have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": --xrwx--x
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 171 /challenge/pwn
You set the correct permissions!
Round 8 of 8!

Current permissions of "/challenge/pwn": --xrwx--x
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": ---rwx--x
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 071 /challenge/pwn
You set the correct permissions!
You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!

Current permissions of "/flag": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ cat /flag
cat: /flag: Permission denied
hacker@permissions~permission-tweaking-practice:~$ chmod cat/flag
chmod: missing operand after ‘cat/flag’
Try 'chmod --help' for more information.
hacker@permissions~permission-tweaking-practice:~$ chmod 400 /flag && stat -c '%A  %a  %U %G  %n' /flag && cat /flag
-r--------  400  hacker hacker  /flag
pwn.college{sZRNeqDpEF1v4KSdyGhqtPj1nn1.QXwEjN0wCNwAzNzEzW}
hacker@permissions~permission-tweaking-practice:~$
```

### New learning
I learnt how to use chmod more effectively.

### References

Chatgpt
******************

## Permission settings practice
Solving a set of questions using chmod.

### Solve
**Flag:**`pwn.college{4KIQB2_uBXt8n1N2_ENOrML7hYu.QXzETO0wCNwAzNzEzW}`

I ran the challenge and and used chmod followed by the number.

```bash
hacker@permissions~permissions-setting-practice:~$ /challenge/run
Round 1 of 8!

Current permissions of "/challenge/pwn": rw-r--r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": ---rwxrwx
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod 077 /challenge/pwn
You set the correct permissions!
Round 2 of 8!

Current permissions of "/challenge/pwn": ---rwxrwx
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rwxrwx--x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod 771 /challenge/pwn
You set the correct permissions!
Round 3 of 8!

Current permissions of "/challenge/pwn": rwxrwx--x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rwxr-xrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod 757 /challenge/pwn
You set the correct permissions!
Round 4 of 8!

Current permissions of "/challenge/pwn": rwxr-xrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rwxrwx-wx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod773 /challenge/pwn
bash: chmod773: command not found
hacker@permissions~permissions-setting-practice:~$ chmod 773 /challenge/pwn
You set the correct permissions!
Round 5 of 8!

Current permissions of "/challenge/pwn": rwxrwx-wx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": ----wx---
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod 030 /challenge/pwn
You set the correct permissions!
Round 6 of 8!

Current permissions of "/challenge/pwn": ----wx---
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw-----wx
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod 603 /challenge/pwn
You set the correct permissions!
Round 7 of 8!

Current permissions of "/challenge/pwn": rw-----wx
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": r--rw-r--
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod 464 /challenge/pwn
You set the correct permissions!
Round 8 of 8!

Current permissions of "/challenge/pwn": r--rw-r--
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw-r-----
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod 640 /challenge/pwn
You set the correct permissions!
You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!

Current permissions of "/flag": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ cat /flag
cat: /flag: Permission denied
hacker@permissions~permissions-setting-practice:~$ chmod 400 cat/flag
chmod: cannot access 'cat/flag': No such file or directory
hacker@permissions~permissions-setting-practice:~$ chmod 400 cat /flag
chmod: cannot access 'cat': No such file or directory
hacker@permissions~permissions-setting-practice:~$ chmod 400 /flag && hexdump -C /flag | sed -n '1,5p' && echo "----" && cat /flag && echo "----" && wc -c /flag && sha256sum /flag && echo "----cleaned----" && tr -d '\r\n' < /flag | xxd -p -c 256 && echo && tr -d '\r\n' < /flag
00000000  70 77 6e 2e 63 6f 6c 6c  65 67 65 7b 34 4b 49 51  |pwn.college{4KIQ|
00000010  42 32 5f 75 42 58 74 38  6e 31 4e 32 5f 45 4e 4f  |B2_uBXt8n1N2_ENO|
00000020  72 4d 4c 37 68 59 75 2e  51 58 7a 45 54 4f 30 77  |rML7hYu.QXzETO0w|
00000030  43 4e 77 41 7a 4e 7a 45  7a 57 7d 0a              |CNwAzNzEzW}.|
0000003c
----
pwn.college{4KIQB2_uBXt8n1N2_ENOrML7hYu.QXzETO0wCNwAzNzEzW}
----
60 /flag
6915730b2e1c476b89714d30b052b07fe42f855620674cbc8d76b90744bbbb29  /flag
----cleaned----
70776e2e636f6c6c6567657b344b495142325f75425874386e314e325f454e4f724d4c376859752e51587a45544f3077434e77417a4e7a457a577d

pwn.college{4KIQB2_uBXt8n1N2_ENOrML7hYu.QXzETO0wCNwAzNzEzW}
```

### New learnings
I learnt how to sue chmod more effectively
### References
Chatgpt
***********************


## The Suid bit

Using chmod u+s to give suid permission.

### Solve
**Flag:**`pwn.college{48BsX0h_Qnn37X5MZ32-vpwCpFv.QXzEjN0wCNwAzNzEzW}`

First chmod u+s to give suid permission to root. 


```bash
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ ls -l
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
hacker@permissions~the-suid-bit:~$ cat /not-the-flag
cat: /not-the-flag: No such file or directory
hacker@permissions~the-suid-bit:~$ cat /flag
cat: /flag: Permission denied
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root!
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{48BsX0h_Qnn37X5MZ32-vpwCpFv.QXzEjN0wCNwAzNzEzW}
```

### New learnings
I learnt how to use chmod u+s to give suid permission

### References
*****************








