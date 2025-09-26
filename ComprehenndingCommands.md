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








