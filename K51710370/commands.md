# K51710370 — Commands
1.Log in to bash <br>
2.To enable the assume_https parameter, type the following command:
```
bash
/usr/share/ts/bin/add_del_internal add assume_https 1
```
3.To restart the BIG-IP ASM services, type the following command:
```
tmsh restart /sys service asm
```
4.To verify the services are in the run state, type the following command:
```
tmsh show /sys service asm
```
The command output appears similar to the following example:
```
asm          run (pid 25144) 10 seconds, 2 starts
```
5.You can disable the assume_https attribute by repeating the three steps previously listed; however, in step 2, you should substitute the value of 0 for 1.
For example:
```
/usr/share/ts/bin/add_del_internal add assume_https 0
```
