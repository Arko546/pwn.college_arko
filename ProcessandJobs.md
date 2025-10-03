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
