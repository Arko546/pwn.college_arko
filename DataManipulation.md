# Data Manipulation

## Translating Characters

Using tr to swap cases.

### Solve
**Flag:**`pwn.college{g22dWpBn9Ik5D9Py9IYPo8VqJo6.01MxEzNxwCNwAzNzEzW}`

I used the tr command piped to the original command to swap the cases of the flag and get the actual one.

```bash
hacker@data~translating-characters:~$ /challenge/run | tr ABCDEFGHIJKLMNOPQR
STUVWXYZabcdefghijklmnopqrstuvwxyz abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNO
PQRSTUVWXYZ
yOUR CASE-SWAPPED FLAG:
pwn.college{g22dWpBn9Ik5D9Py9IYPo8VqJo6.01MxEzNxwCNwAzNzEzW}
```

### New learnings

I learnt how to use the tr command.

### References
*********

## Deleting characters

Using tr to delete characters.

### Solve
**Flag:** `pwn.college{4K2IHYEEXEakptkeTxVAD0jC8W7.0FNxEzNxwCNwAzNzEzW}`

I used tr to remove ^ and %.

```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^
Your character-stuffed flag:
pw%n%.%c%ol%leg%e%{4K2I%H%YE%EXE%a%k%p%tk%e%T%xVA%D0%j%C8%W7%.%0F%N%x%Ez%N%x%wCN%w%A%z%N%zE%z%W%}%
hacker@data~deleting-characters:~$ echo pw%n%.%c%ol%leg%e%{4K2I%H%YE%EXE%a%k%p%tk%e%T%xVA%D0%j%C8%W7%.%0F%N%x%Ez%N%x%wCN%w%A%z%N%zE%z%W%}% | tr -d %
pwn.college{4K2IHYEEXEakptkeTxVAD0jC8W7.0FNxEzNxwCNwAzNzEzW}
```

### New learnings
I learnt how to delete using tr.

### References
*************

## Deleting newlines

Using tr to delete new lines.

### Solve
**Flag:**`pwn.college{E6xsTCbuxgVxkEmxewp1nzWbA3T.0VNxEzNxwCNwAzNzEzW}`

Used the tr command to remove lines.

```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d '\n'
Your line-split flag: pwn.college{E6xsTCbuxgVxkEmxewp1nzWbA3T.0VNxEzNxwCNwAzNzEzW}
```

### New learnings
I learnt how to remove newlines.

### Refernces
**************

## Extracting the first lines with head

I used the hea command to get the first few lines of the input.

### Solve
**Flag:**`pwn.college{UsJaOhUaVhCSvEoV8ik-LiM6OEU.0lNxEzNxwCNwAzNzEzW}`

Using the head to get the first 7 lines and piping it to /challenge/college.

```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{UsJaOhUaVhCSvEoV8ik-LiM6OEU.0lNxEzNxwCNwAzNzEzW}
```

### New learnings
I learnt how to get first few lines of input.

### Refernces
***************

## Extracting specific sections of text

Using cut to get specific columns.

### Solve
**Flag:**`pwn.college{4WCmdRgn4CswrImfEk2torsG2Ol.01NxEzNxwCNwAzNzEzW}`

Using cut to get the column and piping the output to remove the newlines.

```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d ' ' -f2 | tr -d '\n'
pwn.college{4WCmdRgn4CswrImfEk2torsG2Ol.01NxEzNxwCNwAzNzEzW}
```

### New learnings

I learnt how to extract a column using cut.

### References
***************

## Sorting Data

Using sort to sort the data.

### Solve
**Flag:**`pwn.college{IWZ81h4LsPox0kZagc6BskHYM_o.0FM0MDOxwCNwAzNzEzW}`

I read the file and then sorted it in reverse.

```bash
hacker@data~sorting-data:~$ cat /challenge/flags.txt | sort -r
pwn.college{IWZ81h4LsPox0kZagc6BskHYM_o.0FM0MDOxwCNwAzNzEzW}
pwn.college{IWZ81h4LsPox0kZagc6BskHYM_o.0FM0MDOxwCNvAzNzEyW}
pwn.college{IWZ81h4LsPox0kYagc6BrkHYM_o.0FM0LDOxwCNwAzNzEzW}
pwn.college{IWZ81h4KsPox0kZagc6BskHYL_o.0EM0LDNwwCNwAyNzEzW}
pwn.college{IWZ81g4LsPnx0kZagc6BskHYM_o.0FM0MCOxwCMwAzNzEzW}
pwn.college{IWZ81g3LsPox0kZagc6BskHYM_o.0EM0MDOxwCNwAzNzEzW}
pwn.college{IWZ80h3LrPox0kZagc6BskHXM_o.0EL0LCOxwCNwAzNzEzV}
pwn.college{IWZ71h4LrPox0jZafc6AskGYM_o.0FL0MDNxwCNwAzNzEzW}
pwn.college{IWY80h4KrPox0kZagc6BskHXM_n.0FM0MCOxwCNwAzNyEyW}
pwn.college{IVZ81h4LsPox0kZagc6BskHYM_o.0FM0MDOwvCNwAzMzEzW}
pwn.college{IVZ81h4LsPox0kZagc6BsjGYM_o.0EM0LDOxwBNwAyNzEzW}
pwn.college{IVZ81h4LsPox0jZagc5BsjHYM_n.0FM0MDOxwCNwAyMzEzW}
pwn.college{HWZ81h4LsPow0kYafb6BrkGYM_o.0FM0MDOwwBNwAzNzEzW}
pwn.college{HWZ80h4LsPox0kYagc6AskHXM_o.0FM0LCOxwCNwAzNyDyW}
pwn.college{HWY81h3LsPox0kYagc5BrkGYM_o.0EL0MDOxwCNvAzNyEyV}
pwn.collegd{IWZ71h3KrPow0kYagb5BrkHYM_o.0FM0MDOxwCNwAzMzEzW}
pwn.collegd{IWZ70h4LrPnx0jZagc5BskHYM_n.0FM0MDOxwCNwAzMzEyW}
pwn.collefe{IWZ81h4LsPox0kZagc6BskHYM_o.0FM0MDOxwCNwAzNzEzV}
pwn.collefe{IWZ81h4LsPox0jZagc6AskHXM_o.0FL0MDOxwBNwAzNzEzW}
pwn.collefe{IWZ81g4KrPox0kZagc5BsjHXM_o.0FL0MDOxwCNwAyNzEzW}
pwn.collefe{IWY71g4LrOnx0kZagc6BrkHYM_n.0FM0LDOwwCNwAyNzDzV}
pwn.collefd{IWZ81g4LrOnw0kZagb6BrjHYM_o.0FM0MDOxwCNwAzNyEzW}
pwn.colldge{IVZ81h4LsOnx0kZagc6BrkHYM_n.0FM0LDNxwCNwAzNzEzW}
pwn.colldfe{IWZ81h3LrPox0kZagc6AskGXM_o.0FM0LDNxvBNvAzNyEyW}
pwn.colkege{IWZ81h4LrPox0kZagc6AskHYM_o.0FM0MDOxwCNwAzNzEzV}
pwn.colkege{HWZ81h4LsOox0kZagc6BrkHYM_o.0FM0MCOxwCNvAzNzEzW}
pwn.colkege{HWZ70h3LsPow0jZagc5BskHYL_o.0EM0LDNxwBMwAyNzEzW}
pwn.colkegd{IWZ81h4KsPox0kZagc6BsjHYM_o.0FM0MCOxvBMwAzMzEzW}
pwn.colkdfe{IWZ81h4LsPox0kZagb5BskHXL_o.0FL0MDNxwCNwAzNzDyW}
pwn.colkdfe{HVZ80h3LsPox0kYagc6BskHYM_n.0FL0MDOxwCNwAzNzDyV}
pwn.coklege{IWZ81h4LsPox0kZagc6BskGYM_o.0FM0MDOxwCNwAzNzEzW}
pwn.coklege{IWZ81h4KsPow0jZagc6BsjHYM_o.0FM0MCOxwCMwAzMzDyW}
pwn.coklege{HWZ80h4KsOow0kZafc6BsjHXL_o.0EM0LDOwwCNwAzNyEyW}
pwn.coklegd{IWZ80h4LsPox0kZagc5BskHXM_o.0FM0MDOxwCNvAzNzEzW}
pwn.cokldge{HWY81h4LsPnx0jYagc6BsjHXL_n.0EM0MDNxwCNwAyMyEzW}
pwn.cnllege{IWZ81h4LsPox0kZagc6AskHYM_o.0FM0MDOxwCNwAyNzEzW}
pwn.cnllege{IWZ80g4LsPox0kZafc6BskHYM_o.0EM0MCOxwCMwAzMzEyV}
pwn.cnllefe{HWZ71h4KrPow0kZafc6BskHYL_o.0EM0MCNxwCNwAzMyDzV}
pwn.cnlkefe{IWZ81h4KsPox0kYafc5BskHXM_o.0FM0LDOwwBNwAyNyEyV}
pwn.cnlkefe{IWZ81h3LrOox0kZagc6AskHXL_n.0FM0MDNxvCMwAyNzDzW}
pwn.cnklege{IWZ80g4LrPox0kZagc6BskHXM_n.0FM0MDOxwCMwAzNzEzW}
pwn.cnkkege{HVZ81g4LsPox0jYagc6BsjHYM_n.0FM0MCNxvCNwAzNzDzV}
pwn.bollege{IWZ81h4LsPow0jZagb6BskHYM_o.0FM0MDOxwCNwAzNzDzW}
pwn.bollege{IWZ81h4LsOnx0jZagc6BsjGYL_n.0FL0LDOwwBMwAzNyEzW}
pwn.bollege{IWZ71h4LsPnx0jZagc6BskGXM_n.0EM0LCOxwCNvAzNzDzW}
pwn.bollefe{HWZ81h4KsPox0kZagc6BrkHYM_n.0FM0MDOxwCNwAzNzEzW}
pwn.bollefd{IWZ81h4LsPnw0kYagb6AskGXM_o.0EM0MDOwwCMwAzNzDzW}
pwn.bolkdge{IWZ71h4LrPox0kYagc6BskHYM_o.0EM0MDOxwCNwAzMyDyV}
pwn.boklefe{IVZ81g4LsPox0kYagc5ArkGYL_o.0FM0MDOxwCNwAzNzEzW}
pwn.bokldgd{HWY81h4LsPow0kZafc6ArkGYL_o.0FL0MCOwwCMvAyMzEyW}
pwn.bnlkege{IWZ71g4KsPnx0jZafb5AsjHYM_o.0EM0LDOxwCMvAzMzEzW}
pwn.bnlkegd{IWY70h4KsPox0kYagb6ArkGYM_o.0FM0MDOxwCNwAzNyDzW}
pwm.college{HVY80h4LsPox0jZagc6BskHYM_n.0FM0MDNxwCMwAzNzEzV}
pwm.colldge{HWZ81h4LsPox0kZagc6BskHYM_o.0FM0MDOxwCMwAzNzEyW}
pwm.colldge{HWY81h4KsPnx0kZagc6BskHYM_o.0FM0LDOxwBNwAyNyEzW}
pwm.colkegd{IWZ81g4LsPox0kYagc6BskHYM_o.0EM0MDOxwCNwAyNzEzV}
pwm.colkefe{IWZ81h4LsPox0kZafc5BskGYM_o.0FL0MDNxwCNwAzNzEzW}
pwm.cnllege{IVY81h4LsPox0kYagc5AskHXL_o.0FM0MDNxwCNvAyMzEzW}
pwm.cnllege{HWY81h4LsPox0kYafc6AskGYL_o.0FM0MDNxwCMwAyMyEzW}
pwm.cnlkege{IVZ80h3LsOox0jYafb6BsjHYM_o.0EL0LDOxvBMvAzNzEyV}
pwm.cnkldge{HWZ71h4LrPow0kZagb6BskHYM_n.0FM0MCOwwCMwAzNzEzW}
pwm.bollegd{IWZ81h4LsPox0kZagc6BskHYM_o.0FM0MDOxwCNvAzNzEyW}
pwm.bollefe{IWZ81g4LsPox0jZagc6BskHYM_o.0FM0MDNwwCNvAyNzEzW}
debug2: channel 0: window 996681 sent adjust 51895
pwm.bokkdge{HWY81g4KsOox0kZafc5BsjHXL_o.0FM0MCNxvCNwAzNzEzV}
pwm.bnllefd{HVZ81h4LsPnx0kZagc6AsjHYL_n.0FM0MDOxwBNwAzNzEyW}
pwm.bnlldge{IWY80h3KsOow0kYafc6ArkGYM_o.0FM0MDOxwCNwAzNzEzW}
pvn.college{IWZ81h4LsPnx0kZagb6AskHYM_o.0FM0MDOxvBMwAzNzEzW}
pvn.college{IWZ81h3LsPox0kZagc6BsjGYM_o.0FM0MDOwvCNvAzMzEzW}
pvn.college{IVZ70h4KsOow0kYagb5AsjGXM_o.0FM0MCNxwCNvAzMzEzW}
pvn.colldgd{IWZ81h4LsPow0jYagc6BskGYM_o.0FL0MDOxwCNvAzNyEzW}
pvn.colldfd{HVZ70g4KsPox0kYagc6BskGXL_n.0EM0MCOxwCNwAzMyEyW}
pvn.coklefe{HVZ81g4KsPow0kYagb5AsjHYM_o.0FM0MCOxwCNwAyNzEyW}
pvn.cnlldge{IWZ81h4LsPox0kZafb6BskHXM_o.0FM0LDOxwCMwAzNzEzW}
pvn.cnlkegd{IWZ81h4LsPox0jYafc6BskHYM_o.0EM0MCNxwCNwAyMzDzW}
pvn.cnlkegd{IWZ81g4LsPow0kZafc5BskHXM_o.0EM0MDOwwCNwAzMzEzV}
pvn.bolldge{IWZ80h4LrPox0kZagc5AskHYM_n.0EL0MCNxvBNwAyNzDzW}
pvn.bolkefe{HWZ81h4KsPox0kYagc6ArkHYM_o.0FM0LDNxvCNwAyNyEzW}
pvn.bokldfe{IWY70h4LsPox0kYagc5AskHYL_n.0EM0MDOwwBMvAyMzDzW}
pvm.college{IWZ81g4LsPox0kZagc5AskGYM_o.0FM0MDOwwCNwAzNzEyW}
pvm.college{HWZ81h4LsOnx0jZagb6BrkHYM_o.0EM0LDOxwCMvAzNzDzV}
pvm.colkege{IWZ71h4LrOox0jZafc6BskGXM_n.0EM0MDOxwBNvAzNyEzV}
pvm.cnlldfe{HWZ80h3LrPow0kZagb6AskHYM_n.0FL0MDOxwBNwAzMzDzV}
pvm.bollege{IWZ70h4KsOox0kYafb6BsjGYM_n.0FM0LDNxwCNwAzNyDyW}
pvm.bolldgd{IWZ80h4LrPnw0jZagc6AsjGYM_o.0FM0MCOwwBNwAyMzDzW}
pvm.bokkefe{IWY71h3LrPox0jZagb6BskHYM_n.0FM0LCOxwCNvAzNzDzV}
own.college{IWZ81h4LrOox0kZagc6BsjHYL_o.0FM0MDOwwCMwAzNzEzV}
own.collegd{IWY81h4LsPox0kZagc6BskHYM_o.0FM0MDOxwBNwAzNzEzW}
own.collegd{IWY80h4LsPox0kZagc6BskHYL_n.0FM0MDOxwCNvAyMzEzW}
own.collefe{IWZ71g4LsPnw0kZagb5BrjGYM_o.0FM0LDOwwCNvAyNyDzW}
own.colldge{IWZ70g4LsPox0kZagc5BrkGYM_n.0EM0MCOxvCNwAyMzEzW}
own.colkege{IWY81g4KsOox0jYafc6AsjHYM_n.0EM0LDNxwCMvAyMyEyW}
own.bollege{IWY81g3LrPow0kZagc6BskGYL_o.0FM0LDOxwBNwAyNzDzW}
own.boklegd{IWZ81h4KsPnw0kZagc6BrjHXM_o.0FM0MCNxwBNvAzNyEzW}
own.bnklefe{IWY71h3KsPnx0jZagc6ArjHYL_o.0FM0MDNxwBNvAzMzEyW}
owm.colkege{HVY81g4KsPox0kYagc5BskGYM_o.0FM0MCOxvBNwAzNyDzV}
owm.bokkefd{HWZ71h4LsOox0kZafc5BrjHYM_o.0EM0MDNxvBMwAyNzEzW}
ovn.college{IWZ81g4LsPox0kZagc5BskHYM_o.0FM0MDOxwCNwAzNzDyW}
ovn.coklefe{IVZ71h3LrOox0kYagc6BskHYM_o.0EM0LDOxwCNwAzNzDzW}
ovn.cokldgd{IVZ81h4KrOnx0kZafc6BskHYM_o.0FM0MDOxwCNvAzNzEzV}
ovm.college{IWZ81h3LsPox0kZagc6BskHXM_o.0FM0MDOxwBMvAzNyDzW}
ovm.colkdgd{IVZ81h4KrPox0jZagb6BsjGXM_n.0FM0MDOxvCNwAzNzDzW}
```

### New learnings
I learnt how to sort in reverse.

### References
*********

