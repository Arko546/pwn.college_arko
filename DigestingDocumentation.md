# Digesting Documentation 

## Learning from Dcoumentation

Correctly using commands and arguments.

### Solve
**Flag:** `pwn.college{MZnODdg5bV6AX-kEEJTkXVz6QSO.QX0ITO0wCNwAzNzEzW}`

I used the the given command to find the flag.

```bash
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{MZnODdg5bV6AX-kEEJTkXVz6QSO.QX0ITO0wCNwAzNzEzW}
```

### New learnings

I got a better understanding about using commands and arguments.

### Reference 

No reference used
**********

## Learning Complex Usage

Writing an argument in an argument

### Solve
**Flag:** `pwn.college{sZqd7ZnNoyZIyDHI94wJcjDFUon.QX1ITO0wCNwAzNzEzW}`

The /challenge/challenge is a program that allows us to print arbitary files. Using this I used the --printfile argument to print it in the /flag file. Here /flag becomes my argument insde the argument.

```bash
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{sZqd7ZnNoyZIyDHI94wJcjDFUon.QX1ITO0wCNwAzNzEzW}
```

### New learnings 

I learnt how to print a file into another using the printfile.

### Reference

No reference used.
**********

## Reading Manuals

Learn how to use man to read manuals.

### Solve
**Flag:** `pwn.college{YU-H9V3S5V1aW4AQtx277Xf8k4k.QX0EDO0wCNwAzNzEzW}`

I first used the man command to read the manual for challenge. Then I found the argument for challenge that will give me the flag.

```bash
hacker@man~reading-manuals:~$ /challenge/challenge  --atxfkk 935
Correct usage! Your flag: pwn.college{YU-H9V3S5V1aW4AQtx277Xf8k4k.QX0EDO0wCNwAzNzEzW}
```

### New learnings

I learned how to use man command to read the manual for a given command.

### References

No reference used.
*********

## Searching Manuals

Using various commands to navigate in the manual.

### Solve
**Flag:** `pwn.college{odAPe_76J6ot9X6l7WDtv4_jmDT.QX1EDO0wCNwAzNzEzW}`

I first opened the manual using the man command. Then searched for the term flag using / command and found the argument that will give me the flag.

```bash
hacker@man~searching-manuals:~$ /challenge/challenge  --bdtro
Initializing...
Correct usage! Your flag: pwn.college{odAPe_76J6ot9X6l7WDtv4_jmDT.QX1EDO0wCNwAzNzEzW}
```

### New learnings

I learnt how to navigate in the manual.

### References

No reference used.
**********

## Searching for Manuals

Searching for the manual for challenge to find the flag.

### Solve
**Flag:** `pwn.college{8RtZx-CW5cmddVWqa24QtF5u6rH.QX2EDO0wCNwAzNzEzW}`

First I used man man to open the manual for manual. Then  I used the given man -k command to search for the word challenge in all the manuals. This way I found the manual for challenge and found the flag.

```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
txcmddqatu (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man txcmddqatu
hacker@man~searching-for-manuals:~$ /challenge/challenge  --txcmdd 852
Correct usage! Your flag: pwn.college{8RtZx-CW5cmddVWqa24QtF5u6rH.QX2EDO0wCNwAzNzEzW}
```

### New learnings

I learnt more about the man command.

### Refernces

No references used.
***********

## Helpful programs

Learning about help command.

### Solve
**Flag** `pwn.college{QzOVJSWCaW0-N6U5-DlSwUj7jeR.QX3IDO0wCNwAzNzEzW}`

I used the help argument on the challenge command. Then followed the instructions.

```bash
hacker@man~helpful-programs:~$ /challenge/challenge -h
usage: a challenge to make you ask for help [-h] [--fortune] [-v]
                                            [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to
                        give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 65
hacker@man~helpful-programs:~$ /challenge/challenge -g 65
Correct usage! Your flag: pwn.college{QzOVJSWCaW0-N6U5-DlSwUj7jeR.QX3IDO0wCNwAzNzEzW}
```

### New learnings

I learnt how to use hep command.

### References 
No refesnce used
*********

## Help for Builtins

 Learning about builtins in Help

 ### Solve 
 **Flag:** `pwn.college{MjiKsy2pLX1PySDV5GvZvQiVmEz.QX0ETO0wCNwAzNzEzW}`

 I first used help to see all the builtins. Then i used the challenge builtin with help to see whats in it. The i followed the instruction to get the flag.

 ```bash
hacker@man~help-for-builtins:~$ help
GNU bash, version 5.2.37(1)-release (x86_64-pc-linux-gnu)
These shell commands are defined internally.  Type `help' to see this list.
Type `help name' to find out more about the function `name'.
Use `info bash' to find out more about the shell in general.
Use `man -k' or `info' to find out more about commands not in this list.

A star (*) next to a name means that the command is disabled.

 job_spec [&]                          history [-c] [-d offset] [n] or hi>
 (( expression ))                      if COMMANDS; then COMMANDS; [ elif>
 . filename [arguments]                jobs [-lnprs] [jobspec ...] or job>
 :                                     kill [-s sigspec | -n signum | -si>
 [ arg... ]                            let arg [arg ...]
 [[ expression ]]                      local [option] name[=value] ...
 alias [-p] [name[=value] ... ]        logout [n]
 bg [job_spec ...]                     mapfile [-d delim] [-n count] [-O >
 bind [-lpsvPSVX] [-m keymap] [-f fi>  popd [-n] [+N | -N]
 break [n]                             printf [-v var] format [arguments]
 builtin [shell-builtin [arg ...]]     pushd [-n] [+N | -N | dir]
 caller [expr]                         pwd [-LP]
 case WORD in [PATTERN [| PATTERN]..>  read [-ers] [-a array] [-d delim] >
 cd [-L|[-P [-e]] [-@]] [dir]          readarray [-d delim] [-n count] [->
 challenge [--fortune] [--version] [>  readonly [-aAf] [name[=value] ...]>
 command [-pVv] command [arg ...]      return [n]
 compgen [-abcdefgjksuv] [-o option]>  select NAME [in WORDS ... ;] do CO>
 complete [-abcdefgjksuv] [-pr] [-DE>  set [-abefhkmnptuvxBCEHPT] [-o opt>
 compopt [-o|+o option] [-DEI] [name>  shift [n]
 continue [n]                          shopt [-pqsu] [-o] [optname ...]
 coproc [NAME] command [redirections>  source filename [arguments]
 declare [-aAfFgiIlnrtux] [name[=val>  suspend [-f]
 dirs [-clpv] [+N] [-N]                test [expr]
 disown [-h] [-ar] [jobspec ... | pi>  time [-p] pipeline
 echo [-neE] [arg ...]                 times
 enable [-a] [-dnps] [-f filename] [>  trap [-lp] [[arg] signal_spec ...]
 eval [arg ...]                        true
 exec [-cl] [-a name] [command [argu>  type [-afptP] name [name ...]
 exit [n]                              typeset [-aAfFgiIlnrtux] name[=val>
 export [-fn] [name[=value] ...] or >  ulimit [-SHabcdefiklmnpqrstuvxPRT]>
 false                                 umask [-p] [-S] [mode]
 fc [-e ename] [-lnr] [first] [last]>  unalias [-a] name [name ...]
 fg [job_spec]                         unset [-f] [-v] [-n] [name ...]
 for NAME [in WORDS ... ] ; do COMMA>  until COMMANDS; do COMMANDS-2; do>
 for (( exp1; exp2; exp3 )); do COMM>  variables - Names and meanings of >
 function name { COMMANDS ; } or nam>  wait [-fn] [-p var] [id ...]
 getopts optstring name [arg ...]      while COMMANDS; do COMMANDS-2; do>
 hash [-lr] [-p pathname] [-dt] [nam>  { COMMANDS ; }
 help [-dms] [pattern ...]
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "MjiKsy2p".
hacker@man~help-for-builtins:~$ challenge --secret MjiKsy2p
Correct! Here is your flag!
pwn.college{MjiKsy2pLX1PySDV5GvZvQiVmEz.QX0ETO0wCNwAzNzEzW}
```

### New learnings

I learnt about finding builtins in the the help command.

### References

No references used.
***********





