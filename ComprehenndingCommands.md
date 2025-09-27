# Comprehending Commands

## cat: not the pet, but the command!

Different functions of cat command.

### Solve
**Flag** `pwn.college{gB1DuiRaEz0TgDBqCCwYST77pBI.QXxcTN0wCNwAzNzEzW}`

Reading the file using cat command.

```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{gB1DuiRaEz0TgDBqCCwYST77pBI.QXxcTN0wCNwAzNzEzW}
```

### New learnings
I learnt that cat function helps us read files. We can also concatenate different files by writing them one after the other. 

### References
No reference used

********

## catting absolute paths

Reading the files using absolute path after cat command.

### Solve
**Flag** `pwn.college{0vKzTMAsd3UUlJUgQ0Qa2MmSAf2.QX5ETO0wCNwAzNzEzW}`

Reading the file using cat command.

```bash
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{0vKzTMAsd3UUlJUgQ0Qa2MmSAf2.QX5ETO0wCNwAzNzEzW}
```

### New learnings

I learnt that cat function can read file using absolute path as arguments.

### References

No referecnce used

********

## catting absolute paths

Reading the files using absolute path after cat command.

### Solve
**Flag** `pwn.college{0vKzTMAsd3UUlJUgQ0Qa2MmSAf2.QX5ETO0wCNwAzNzEzW}`

Reading the file using cat command.

```bash
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{0vKzTMAsd3UUlJUgQ0Qa2MmSAf2.QX5ETO0wCNwAzNzEzW}
```

### New learnings

I learnt that cat function can read file using absolute path as arguments.

### References

No referecnce used
********

## more catting practise

Finding flag using cat to read absolute path

### Solve
**Flag** `pwn.college{o9hsl3dX3Ei___r5PbgXuPARAGf.QXwITO0wCNwAzNzEzW}`

Reading the file using cat command

```bash
hacker@commands~more-catting-practice:~$ cat /lib/x86_64-linux-gnu/rsocket/flag
pwn.college{o9hsl3dX3Ei___r5PbgXuPARAGf.QXwITO0wCNwAzNzEzW}
```

### New learnings

I practised using cat command with a absolute path as an argument.

### References

No reference used
*******

## grepping for a needle in a haystack

Finding files by searching for the contents in it using grep function.

### Solve
**Flag** `pwn.college{8KSA2zG9YCyCYvLbhOLjmfNxD-7.QX3EDO0wCNwAzNzEzW}`

I used the grep command to search for pwn.college as i know it is common in all flags and wrote the absolute path of the directory under which the file is included.

```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /cha
llenge/data.txt
pwn.college{8KSA2zG9YCyCYvLbhOLjmfNxD-7.QX3EDO0wCNwAzNzEzW}
```

### New learnings

I learnt how to search for a file by entering the contents using the grep command.

### Resources

No reference used
**********

## comparing files

Finding the flag by comparing two files.

### Solve
**Flag** `pwn.college{44bRHZbzwNgDz1Ok3DzBy1WZL6p.01MwMDOxwCNwAzNzEzW}`

First used cat command to read the two files. Then using diff to compare them and find out the flag.

```bash
hacker@commands~comparing-files:~$ cat /challenge/decoys_only.txt
pwn.college{fake_flag_number_1_bfWxpkdNiAc}
pwn.college{fake_flag_number_2_m9W2edK8Ao0}
pwn.college{fake_flag_number_3_kfHlIbOe6wI}
pwn.college{fake_flag_number_4_zmgcI3M2zBM}
pwn.college{fake_flag_number_5_G1ttXpDc8OE}
pwn.college{fake_flag_number_6_pIlm0GaO0s8}
pwn.college{fake_flag_number_7_mbte4E4Qn0}
pwn.college{fake_flag_number_8_i6QvjBFH4oA}
pwn.college{fake_flag_number_9_7lI0fE8BBC8}
pwn.college{fake_flag_number_10_i2Q9YvKYXGM}
pwn.college{fake_flag_number_11_zhrWJU6qE2g}
pwn.college{fake_flag_number_12_mh9ZqM3djE}
pwn.college{fake_flag_number_13_zEOCRbIQA}
pwn.college{fake_flag_number_14_L7JlD88X4M}
pwn.college{fake_flag_number_15_MvquZK5R5Jo}
pwn.college{fake_flag_number_16_HRgUFPuVbto}
pwn.college{fake_flag_number_17_DrxuN27EY24}
pwn.college{fake_flag_number_18_JCJuqhl3F5Y}
pwn.college{fake_flag_number_19_BRyVmZT7Yk}
pwn.college{fake_flag_number_20_7OHbiCwA3g4}
pwn.college{fake_flag_number_21_jwb5rWITqDw}
pwn.college{fake_flag_number_22_ZTJLItBOZFU}
pwn.college{fake_flag_number_23_OUznYMvjSHQ}
pwn.college{fake_flag_number_24_utfhituRHic}
pwn.college{fake_flag_number_25_q6E7kEl0M}
pwn.college{fake_flag_number_26_JBGcHfC2yyo}
pwn.college{fake_flag_number_27_AMOalhoSVNg}
pwn.college{fake_flag_number_28_K8ALqhAs7uI}
pwn.college{fake_flag_number_29_7SWCKPVnFmg}
pwn.college{fake_flag_number_30_IDfgcPi9Gr8}
pwn.college{fake_flag_number_31_IFoa0zVRfW0}
pwn.college{fake_flag_number_32_m5hygLNyfk}
pwn.college{fake_flag_number_33_HHzDltupHak}
pwn.college{fake_flag_number_34_vkwKpNDV4eA}
pwn.college{fake_flag_number_35_xyghnFPuuQ}
pwn.college{fake_flag_number_36_3CYZXGHcQAQ}
pwn.college{fake_flag_number_37_jl2GUzLGcRM}
pwn.college{fake_flag_number_38_73UAMi07f4}
pwn.college{fake_flag_number_39_b1a2RiawOM}
pwn.college{fake_flag_number_40_1RmV1N2LM}
pwn.college{fake_flag_number_41_MHoVkK4Hfw}
pwn.college{fake_flag_number_42_X9YaKYyihU}
pwn.college{fake_flag_number_43_JwkWKToWvD0}
pwn.college{fake_flag_number_44_EdPS41JMMN4}
pwn.college{fake_flag_number_45_djJqgcgRGb0}
pwn.college{fake_flag_number_46_1pBXNlXaKA}
pwn.college{fake_flag_number_47_vJ1kRSDdMuI}
pwn.college{fake_flag_number_48_1mXg1OySznY}
pwn.college{fake_flag_number_49_lfh1uT9Evv8}
pwn.college{fake_flag_number_50_bjGNW5yNkNs}
pwn.college{fake_flag_number_51_76qp7J8rIY}
pwn.college{fake_flag_number_52_eCnP7o6bRXI}
pwn.college{fake_flag_number_53_62lP07IILa0}
pwn.college{fake_flag_number_54_MOQcgWRyDbM}
pwn.college{fake_flag_number_55_NOg9z3dAX0}
pwn.college{fake_flag_number_56_4q3yCwnPF4}
pwn.college{fake_flag_number_57_9bVIaJFvoU}
pwn.college{fake_flag_number_58_vFgmMkKHB2M}
pwn.college{fake_flag_number_59_WMJ8ihGA4g}
pwn.college{fake_flag_number_60_6OH21AefrbM}
pwn.college{fake_flag_number_61_WX5M5Df6s}
pwn.college{fake_flag_number_62_xcnHFeRIytM}
pwn.college{fake_flag_number_63_Rl0pTiKuxo}
pwn.college{fake_flag_number_64_cJrsPzxjlsY}
pwn.college{fake_flag_number_65_xL3K0anDjTY}
pwn.college{fake_flag_number_66_Kwc4UMo2GFw}
pwn.college{fake_flag_number_67_e805QcAHPYw}
pwn.college{fake_flag_number_68_J61LfqCW7AY}
pwn.college{fake_flag_number_69_xHR3VnVpsAg}
pwn.college{fake_flag_number_70_DeA9rzQ0MRQ}
pwn.college{fake_flag_number_71_kbVvimxUAE}
pwn.college{fake_flag_number_72_zdKlDqr2tQI}
pwn.college{fake_flag_number_73_Vnl0Ok05TvQ}
pwn.college{fake_flag_number_74_furp3VMpHsM}
pwn.college{fake_flag_number_75_hSQuWL3n8Y4}
pwn.college{fake_flag_number_76_bzxWrxXj75w}
pwn.college{fake_flag_number_77_yL0fQxNCKe0}
pwn.college{fake_flag_number_78_lsdVUumFI5k}
pwn.college{fake_flag_number_79_ezfbW9i1cg}
pwn.college{fake_flag_number_80_bk1SOos4Pgw}
pwn.college{fake_flag_number_81_5q4io6ORQ00}
pwn.college{fake_flag_number_82_S5JGi8kFUY}
pwn.college{fake_flag_number_83_UuI9YNdEyiE}
pwn.college{fake_flag_number_84_57riAukKfU}
pwn.college{fake_flag_number_85_FuCUCGu8LHI}
pwn.college{fake_flag_number_86_T1cQ3mMrJjc}
pwn.college{fake_flag_number_87_x7Uul9lIgu8}
pwn.college{fake_flag_number_88_Ovso9CwiVFI}
pwn.college{fake_flag_number_89_a9MBA8a7vFM}
pwn.college{fake_flag_number_90_0kNrJtGDdxU}
pwn.college{fake_flag_number_91_0xDL9rbtiwg}
pwn.college{fake_flag_number_92_uhhFrdh7Yk}
pwn.college{fake_flag_number_93_IGm5IxeFaN8}
pwn.college{fake_flag_number_94_rte7K72U8s}
pwn.college{fake_flag_number_95_84NWqAbAgVg}
pwn.college{fake_flag_number_96_JWPBCm0jFbk}
pwn.college{fake_flag_number_97_JH6Xj6bbYmI}
pwn.college{fake_flag_number_98_G1xqo9fEcOc}
pwn.college{fake_flag_number_99_Z676nyqAky0}
pwn.college{fake_flag_number_100_RSeLa1aXqAs}
hacker@commands~comparing-files:~$ cat /challenge/decoys_and_real.txt
pwn.college{fake_flag_number_1_bfWxpkdNiAc}
pwn.college{fake_flag_number_2_m9W2edK8Ao0}
pwn.college{fake_flag_number_3_kfHlIbOe6wI}
pwn.college{fake_flag_number_4_zmgcI3M2zBM}
pwn.college{fake_flag_number_5_G1ttXpDc8OE}
pwn.college{fake_flag_number_6_pIlm0GaO0s8}
pwn.college{fake_flag_number_7_mbte4E4Qn0}
pwn.college{fake_flag_number_8_i6QvjBFH4oA}
pwn.college{fake_flag_number_9_7lI0fE8BBC8}
pwn.college{fake_flag_number_10_i2Q9YvKYXGM}
pwn.college{fake_flag_number_11_zhrWJU6qE2g}
pwn.college{fake_flag_number_12_mh9ZqM3djE}
pwn.college{fake_flag_number_13_zEOCRbIQA}
pwn.college{fake_flag_number_14_L7JlD88X4M}
pwn.college{fake_flag_number_15_MvquZK5R5Jo}
pwn.college{fake_flag_number_16_HRgUFPuVbto}
pwn.college{fake_flag_number_17_DrxuN27EY24}
pwn.college{fake_flag_number_18_JCJuqhl3F5Y}
pwn.college{fake_flag_number_19_BRyVmZT7Yk}
pwn.college{fake_flag_number_20_7OHbiCwA3g4}
pwn.college{fake_flag_number_21_jwb5rWITqDw}
pwn.college{fake_flag_number_22_ZTJLItBOZFU}
pwn.college{fake_flag_number_23_OUznYMvjSHQ}
pwn.college{fake_flag_number_24_utfhituRHic}
pwn.college{fake_flag_number_25_q6E7kEl0M}
pwn.college{fake_flag_number_26_JBGcHfC2yyo}
pwn.college{fake_flag_number_27_AMOalhoSVNg}
pwn.college{fake_flag_number_28_K8ALqhAs7uI}
pwn.college{fake_flag_number_29_7SWCKPVnFmg}
pwn.college{fake_flag_number_30_IDfgcPi9Gr8}
pwn.college{fake_flag_number_31_IFoa0zVRfW0}
pwn.college{fake_flag_number_32_m5hygLNyfk}
pwn.college{fake_flag_number_33_HHzDltupHak}
pwn.college{fake_flag_number_34_vkwKpNDV4eA}
pwn.college{fake_flag_number_35_xyghnFPuuQ}
pwn.college{fake_flag_number_36_3CYZXGHcQAQ}
pwn.college{fake_flag_number_37_jl2GUzLGcRM}
pwn.college{fake_flag_number_38_73UAMi07f4}
pwn.college{fake_flag_number_39_b1a2RiawOM}
pwn.college{fake_flag_number_40_1RmV1N2LM}
pwn.college{fake_flag_number_41_MHoVkK4Hfw}
pwn.college{fake_flag_number_42_X9YaKYyihU}
pwn.college{fake_flag_number_43_JwkWKToWvD0}
pwn.college{fake_flag_number_44_EdPS41JMMN4}
pwn.college{fake_flag_number_45_djJqgcgRGb0}
pwn.college{fake_flag_number_46_1pBXNlXaKA}
pwn.college{44bRHZbzwNgDz1Ok3DzBy1WZL6p.01MwMDOxwCNwAzNzEzW}
pwn.college{fake_flag_number_47_vJ1kRSDdMuI}
pwn.college{fake_flag_number_48_1mXg1OySznY}
pwn.college{fake_flag_number_49_lfh1uT9Evv8}
pwn.college{fake_flag_number_50_bjGNW5yNkNs}
pwn.college{fake_flag_number_51_76qp7J8rIY}
pwn.college{fake_flag_number_52_eCnP7o6bRXI}
pwn.college{fake_flag_number_53_62lP07IILa0}
pwn.college{fake_flag_number_54_MOQcgWRyDbM}
pwn.college{fake_flag_number_55_NOg9z3dAX0}
pwn.college{fake_flag_number_56_4q3yCwnPF4}
pwn.college{fake_flag_number_57_9bVIaJFvoU}
pwn.college{fake_flag_number_58_vFgmMkKHB2M}
pwn.college{fake_flag_number_59_WMJ8ihGA4g}
pwn.college{fake_flag_number_60_6OH21AefrbM}
pwn.college{fake_flag_number_61_WX5M5Df6s}
pwn.college{fake_flag_number_62_xcnHFeRIytM}
pwn.college{fake_flag_number_63_Rl0pTiKuxo}
pwn.college{fake_flag_number_64_cJrsPzxjlsY}
pwn.college{fake_flag_number_65_xL3K0anDjTY}
pwn.college{fake_flag_number_66_Kwc4UMo2GFw}
pwn.college{fake_flag_number_67_e805QcAHPYw}
pwn.college{fake_flag_number_68_J61LfqCW7AY}
pwn.college{fake_flag_number_69_xHR3VnVpsAg}
pwn.college{fake_flag_number_70_DeA9rzQ0MRQ}
pwn.college{fake_flag_number_71_kbVvimxUAE}
pwn.college{fake_flag_number_72_zdKlDqr2tQI}
pwn.college{fake_flag_number_73_Vnl0Ok05TvQ}
pwn.college{fake_flag_number_74_furp3VMpHsM}
pwn.college{fake_flag_number_75_hSQuWL3n8Y4}
pwn.college{fake_flag_number_76_bzxWrxXj75w}
pwn.college{fake_flag_number_77_yL0fQxNCKe0}
pwn.college{fake_flag_number_78_lsdVUumFI5k}
pwn.college{fake_flag_number_79_ezfbW9i1cg}
pwn.college{fake_flag_number_80_bk1SOos4Pgw}
pwn.college{fake_flag_number_81_5q4io6ORQ00}
pwn.college{fake_flag_number_82_S5JGi8kFUY}
pwn.college{fake_flag_number_83_UuI9YNdEyiE}
pwn.college{fake_flag_number_84_57riAukKfU}
pwn.college{fake_flag_number_85_FuCUCGu8LHI}
pwn.college{fake_flag_number_86_T1cQ3mMrJjc}
pwn.college{fake_flag_number_87_x7Uul9lIgu8}
pwn.college{fake_flag_number_88_Ovso9CwiVFI}
pwn.college{fake_flag_number_89_a9MBA8a7vFM}
pwn.college{fake_flag_number_90_0kNrJtGDdxU}
pwn.college{fake_flag_number_91_0xDL9rbtiwg}
pwn.college{fake_flag_number_92_uhhFrdh7Yk}
pwn.college{fake_flag_number_93_IGm5IxeFaN8}
pwn.college{fake_flag_number_94_rte7K72U8s}
pwn.college{fake_flag_number_95_84NWqAbAgVg}
pwn.college{fake_flag_number_96_JWPBCm0jFbk}
pwn.college{fake_flag_number_97_JH6Xj6bbYmI}
pwn.college{fake_flag_number_98_G1xqo9fEcOc}
pwn.college{fake_flag_number_99_Z676nyqAky0}
pwn.college{fake_flag_number_100_RSeLa1aXqAs}
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
46a47
> pwn.college{44bRHZbzwNgDz1Ok3DzBy1WZL6p.01MwMDOxwCNwAzNzEzW}
```

### New learnings

I learnt about using diff command to compare two similar files.

### References

No references used.
**********

## listing files

Using ls to find files in a directory.

### Solve
**Flag** `pwn.college{gHHm0oL33-HR6h1Kzc_aGCIp0J_.QX4IDO0wCNwAzNzEzW}`

I used the ls command followed by the challenge directory to look at all the files in the directory. Then i executed the the run file that was renamed something else using absolute path.

```bash
hacker@commands~listing-files:~$ ls /challenge
583-renamed-run-17426  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/583-renamed-run-17426
Yahaha, you found me! Here is your flag:
pwn.college{gHHm0oL33-HR6h1Kzc_aGCIp0J_.QX4IDO0wCNwAzNzEzW}
```
### New learnings

I learnt how to list the files under a directory.

### References

No reference used.
*********

## touching files

Using touch command to create new files.

### Solve
**Flag** `pwn.college{80ZIArSMxqkYI8vgWzTn2EGaEEP.QXwMDO0wCNwAzNzEzW}`

I used the touch command to create two files in the tmp directory. Then used the absolute path to find the flag.

```bash

hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{80ZIArSMxqkYI8vgWzTn2EGaEEP.QXwMDO0wCNwAzNzEzW}

```

### Neew learnings

I learnt how to create files using the touch command.

### References

No reference used
**********

## Removing Files

Removing files using rm command.

### Solve
**Flag** `pwn.college{kDf1MahUWDPHugNvXwT4QwZKYIp.QX2kDM1wCNwAzNzEzW}`

I created the delete_me file using touch. Then deleted it using rm command. Then ran the given command to get the flag.

```bash
hacker@commands~removing-files:~$ touch delete_me
hacker@commands~removing-files:~$ ls
a  delete_me
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ ls
a
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{kDf1MahUWDPHugNvXwT4QwZKYIp.QX2kDM1wCNwAzNzEzW}
```

### New learnings

I learnt how to use the rm command to delete files.

### References

No refernece used.

*******

## Moving files

Moves the files from one directory to other

### Solve
**Flag** `pwn.college{EEHptiu44msoUTTxYDzY-McwxnC.0VOxEzNxwCNwAzNzEzW}`

I used the mv command to move the /flag file to the given directory.

```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{EEHptiu44msoUTTxYDzY-McwxnC.0VOxEzNxwCNwAzNzEzW}
```

### New Learnings 

I learnt how to move files using the mv command.

### References

No reference used.
*******

## hidden files

Finding files that are not visible using the ls command.

### Solve
**Flag:** `pwn.college{4_S5qG60rnHQ-Ycj0lWewpZIxZq.QXwUDO0wCNwAzNzEzW}`

I first moved into the / directory using the cd command. Then I used the ls -a command to find see all the files including the ones starting with a '.'. Then I tried to run the file directly but I was denied access. So I used the cat command to read inside the file and found the flag. 

```bash
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.                      bin        etc    lib64   nix   run   tmp
..                     boot       home   libx32  opt   sbin  usr
.dockerenv             challenge  lib    media   proc  srv   var
.flag-201452146727600  dev        lib32  mnt     root  sys
hacker@commands~hidden-files:/$ /.flag-201452146727600
bash: /.flag-201452146727600: Permission denied
hacker@commands~hidden-files:/$ cat /.flag-201452146727600
pwn.college{4_S5qG60rnHQ-Ycj0lWewpZIxZq.QXwUDO0wCNwAzNzEzW}
```

### New learnings

I learnt how to see files that are hidden because they start with a '.' using the ls -a command.

### References
No reference used.

## An epic filesystem quest

Finding the flag by following the given instruction.

### Solve 
**Flag** `pwn.college{YCAECYIX3kJfL6y7bsQoBRCUod-.QX5IDO0wCNwAzNzEzW}`

I used the cd command to navigate to different directories. I then used the ls or ls -a to view the files in the directories. I then used the cat command to read the files and go to the next durectory. There were some hints that required me to use ls -a and cat directly followed by the absolute path. I finally found the flag after following all the rules. 

```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
MESSAGE  challenge  flag  lib32   media  opt   run   sys  var
bin      dev        home  lib64   mnt    proc  sbin  tmp
boot     etc        lib   libx32  nix    root  srv   usr
hacker@commands~an-epic-filesystem-quest:/$ cat MESSAGE
Lucky listing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/jupyter_server/view
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/local/lib/python3.8/dist
-packages/jupyter_server/view
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jupyter_server/view$ ls
DISPATCH  __init__.py  __pycache__  handlers.py
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jupyter_server/view$ cat DISPATCH
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/include/crypto/internal
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jupyter_server/view$ cd /opt/linux/linux-5.4/include/crypto/internal
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/crypto/internal$ ls
NOTE         akcipher.h    geniv.h  rng.h        simd.h
acompress.h  cryptouser.h  hash.h   rsa.h        skcipher.h
aead.h       des.h         kpp.h    scompress.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/crypto/internal$ cat NOTE
Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/Crypto/SelfTest/__pycache__

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/crypto/internal$ ls /usr/local/lib/python3.8/dist-packages/Crypto/SelfTest/__pycache__
CLUE-TRAPPED             __main__.cpython-38.pyc  st_common.cpython-38.pyc
__init__.cpython-38.pyc  loader.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/crypto/internal$ cat /usr/local/lib/python3.8/dist-packages/Crypto/SelfTest/__pycache__/CLUE-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/lib/python3/dist-packages/matplotlib/testing/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/crypto/internal$ ls -a /usr/lib/python3/dist-packages/matplotlib/testing/__pycache__
.                        conftest.cpython-38.pyc
..                       decorators.cpython-38.pyc
.TRACE                   determinism.cpython-38.pyc
__init__.cpython-38.pyc  disable_internet.cpython-38.pyc
compare.cpython-38.pyc   exceptions.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/crypto/internal$ cat  /usr/lib/python3/dist-packages/matplotlib/testing/__pycache__/.TRACE
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/virtual
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/crypto/internal$ cd /opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/virtual
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/virtual$ ls
GIST      virtual_link_encoder.c  virtual_stream_encoder.c
Makefile  virtual_link_encoder.h  virtual_stream_encoder.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/virtual$ cat GIST
Congratulations, you found the clue!
The next clue is in: /usr/share/racket/pkgs/games/paint-by-numbers/raw-problems/compiled

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/virtual$ ls -a  /usr/share/racket/pkgs/games/paint-by-numbers/raw-problems/compiled
.                            raw-hattori_rkt.dep
..                           raw-hattori_rkt.zo
.POINTER                     raw-kajitani_rkt.dep
build-final_rkt.dep          raw-kajitani_rkt.zo
build-final_rkt.zo           raw-misc_rkt.dep
build-hattori_rkt.dep        raw-misc_rkt.zo
build-hattori_rkt.zo         raw-problems_rkt.dep
build-rows-cols_rkt.dep      raw-problems_rkt.zo
build-rows-cols_rkt.zo       size-calculation_rkt.dep
build-solution-sets_rkt.dep  size-calculation_rkt.zo
build-solution-sets_rkt.zo
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/virtual$ cat  /usr/share/racket/pkgs/games/paint-by-numbers/raw-problems/compiled/.POINTER
Congratulations, you found the clue!
The next clue is in: /usr/share/locale/io/LC_MESSAGES

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/virtual$ cd /usr/share/locale/io/LC_MESSAGES
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/io/LC_MESSAGES$ ls
EVIDENCE  iso_3166-1.mo  iso_3166.mo
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/io/LC_MESSAGES$ cat EVIDENCE
Lucky listing!
The next clue is in: /usr/share/doc/libpcrecpp0v5

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/io/LC_MESSAGES$ cd /usr/share/doc/libpcrecpp0v5
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libpcrecpp0v5$ ls
AUTHORS  DOSSIER  NEWS.gz  README.gz  changelog.Debian.gz  copyright
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/libpcrecpp0v5$ cat DOSSIER
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{YCAECYIX3kJfL6y7bsQoBRCUod-.QX5IDO0wCNwAzNzEzW}
```
### New Leearnings

I learnt how to effectively use cd, cat and ls commands.

### References
No references used.
***************

## making directories

Using mkdir to makae new directories/

### Solve
**Flag:** `pwn.college{k3nSyrPXYQs5_3OUtI0gVUT2HpT.QXxMDO0wCNwAzNzEzW}`

First I made a directory in tmp using mkdir command. Then I made a file using touch inside the directory. 

```bash
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ touch /tmp/pwn/college
hacker@commands~making-directories:~$ /challenge/run
Success! Here is your flag:
pwn.college{k3nSyrPXYQs5_3OUtI0gVUT2HpT.QXxMDO0wCNwAzNzEzW}
```

### New learnings

I learnt how to make a directory.

### References

No reference used
**********


## Findings files

Using find command to find the flag.

### Solve
**Flag** `pwn.college{oSuK12_Pcfr30EqW3TydWYAdfmx.QXyMDO0wCNwAzNzEzW}`

First I searched for files or directories named flag using the find command. Then all absolute paths that led to files containing the word flag were shown. I used the cat command to read the files and find the flag.

```bash

hacker@commands~finding-files:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/tmp/tmp.4mK6TfTSUV’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/7/task/7/fd’: Permission denied
find: ‘/proc/7/task/7/fdinfo’: Permission denied
find: ‘/proc/7/task/7/ns’: Permission denied
find: ‘/proc/7/fd’: Permission denied
find: ‘/proc/7/map_files’: Permission denied
find: ‘/proc/7/fdinfo’: Permission denied
find: ‘/proc/7/ns’: Permission denied
/opt/linux/linux-5.4/tools/build/feature/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag
/nix/store/h88mxp2mbgyj06vypwmqpy05idhwimnp-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag
/nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag
/nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /opt/linux/linux-5.4/tools/build/feature/flag
pwn.college{oSuK12_Pcfr30EqW3TydWYAdfmx.QXyMDO0wCNwAzNzEzW}
```

### New learnings

I learnt how to search for files with a particular name using he find command.

### References 

No reference used.
*********

## Linking files

Using ln function to link files

### Solve
**Flag:** `pwn.college{EKWD4k5KE1sWd82pC7JSxvjhl_P.QX5ETN1wCNwAzNzEzW}`

I first linked the flag to to /not-the-flag file. Then the /challenge/catflag is programmed to read the /not-the-flag file so i ran it and got the flag.

``` bash
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challgenge/catflag /home/hacker/not-the-flag
bash: /challgenge/catflag: No such file or directory
hacker@commands~linking-files:~$ /challenge/catflag /home/hacker/not-the-fla
g
About to read out the /home/hacker/not-the-flag file!
pwn.college{EKWD4k5KE1sWd82pC7JSxvjhl_P.QX5ETN1wCNwAzNzEzW}
```

### New learnings

I learnt how to link files using the the ln and ln -s. I also learnt about hard and soft links.

### Refernces 
No reference used.

*********












