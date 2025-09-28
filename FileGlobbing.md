# File Globbing

## Matching with *

Uaing * to glob.

### Solve
**Flag** `pwn.college{wBYwkfCKeeDbQ64ziK4EdIbsoWO.QXxIDO0wCNwAzNzEzW}`

I used the * to glob challenge and the give absolute path to get flag.

```bash
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{wBYwkfCKeeDbQ64ziK4EdIbsoWO.QXxIDO0wCNwAzNzEzW}
```

### New learning
I learnt how to use * to glob.

### Reference
********

## Matching with ?

Uaing ? to match individual characters.

### Solve
**Flag** `pwn.college{YcBqOztKKpNWi9ZENBQ_8upNV4U.QXyIDO0wCNwAzNzEzW}`

I used the ? to to fill for individual characters. And then find the flag.
```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{YcBqOztKKpNWi9ZENBQ_8upNV4U.QXyIDO0wCNwAzNzEzW}
```

### New learning
I learnt how to use ? to replace individual characters.

### Reference 
No reference used.
**********

## Mtching with []

Using [] to look for multiple characters.

### Solve
**Flag:** `pwn.college{88NH5Ts56TVyyFQwXLvQ7UCZhc7.QXzIDO0wCNwAzNzEzW}`

I first moved in to the given directory. From there I used the [] command to search for names that end with the given letters.
```bash

hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{88NH5Ts56TVyyFQwXLvQ7UCZhc7.QXzIDO0wCNwAzNzEzW}
```

### New learnings

I learnt how to use [].

### Refernces

No references used.
*************

## Matching paths with []

Using [] in an absolute path.

### Solve
**Flag** `pwn.college{MJQ1ejca76fd0-6wvTJDTeXKKZs.QX0IDO0wCNwAzNzEzW}`

Used a direct path and [] to match with the file names which end with those letters.

```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[absh]
You got it! Here is your flag!
pwn.college{MJQ1ejca76fd0-6wvTJDTeXKKZs.QX0IDO0wCNwAzNzEzW}
```

### New learnings

I learnt how to use absolute patha and [] together.

### References

***************

## Multiple globs

Using multiple globs in one command

###  Solve
**Flag:** `pwn.college{k52XLYgpUZiJoD0BRAnJ3rIR9kv.0lM3kjNxwCNwAzNzEzW}`

Used * at start and end because we dont know the first and last terms and the only letter we know is p.

```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{k52XLYgpUZiJoD0BRAnJ3rIR9kv.0lM3kjNxwCNwAzNzEzW}
```

### New learnings

I learnt how to use multiple globs at once.

### Reference
*************

## Mixing globs
Using two different globs together.

### Solve
**Flag:** `pwn.college{0lWUrElJsW4FolhzkYdBWBP1hHa.QX1IDO0wCNwAzNzEzW}`

I used the square bracket glob to include the initial letters and followed it with star as it continued to some letters.

```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{0lWUrElJsW4FolhzkYdBWBP1hHa.QX1IDO0wCNwAzNzEzW}
```

### New learnings
I learnt how to use different kinds of globs together.

### Refererences

No references used.
**********

## Exclusionary globbing

Using ! to exclude characters in a square bracket glob.

### Solve
**Flag:** `pwn.college{Ysi-uE1QtfQwABzEBk5lf0sYc-H.QX2IDO0wCNwAzNzEzW}`

I used the ! in a square glob to exclude all characters starting with those letters. Then I put * after for the rest of the letters.

```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{Ysi-uE1QtfQwABzEBk5lf0sYc-H.QX2IDO0wCNwAzNzEzW}
```

### New learnings

I learnt about using ! .

### References
No referneces.
**********

## Tab completion
Using tab to finish the command

### Solve
**Flag:** `pwn.college{QLFKRSfakQImJihhNFqzk2U0TKH.0FN0EzNxwCNwAzNzEzW}`

Typed the initial few characters then tab to complete the directory.

```bash
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​
pwn.college{QLFKRSfakQImJihhNFqzk2U0TKH.0FN0EzNxwCNwAzNzEzW}
```

### New learnings
I learnt about autocompleting with the tab key.

### References
No reference used.
**************

## Multiple options for tab completion

Finding the file using flag when multiple have same initials.

### Solve
**Flag:** `pwn.college{0kH-3GelmHc2qyF_o1A_5WMtSNK.0lN0EzNxwCNwAzNzEzW}`

I first wrote the given path and then used tab to circle to pwn. Then on pressing tab again I got a list of files with the pwn as the initials.

```bash



