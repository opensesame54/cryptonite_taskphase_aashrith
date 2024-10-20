# Perceiving Permissions Module 
### Changing File Ownership 
```
This teaches us the use of the chown (change ownership) command. In this challenge, we change the ownership of the flag file to hacker and initialize it to get the flag.
flag=pwn.college{UtSwUl10bK2VcURWjCIK97HydcC.dFTM2QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/e3f09022-4c51-4a17-b061-e851ad63fc11)

### Groups and Files 
```
In this challenge, we change the group of the flag file as the hacker user using the chgrp and then cat the flag file to get the flag. 
flag=pwn.college{YNgXL2rVrs-rM3c2vLEBUzMHRFg.dFzNyUDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/05fdd62c-ef8a-4ecf-96ee-44e8634658f1)

### Fun with groups Names 
```
First, we run id to get the name of the group we have to change the flag file and then cat the flag. 
flag=pwn.college{IdtO5JFfClpVS0rc501_20BfBho.dJzNyUDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/65d1b2f9-59d9-459d-ad76-9892b9f9fb05)

### Changing Permissions 
```
In this challenge, we use the chmod command to change the permissions of the flag file. So we use chmod o+r /flag, so that other users can also get 
access to the flag file, then we can get access to the flag file using cat. 
flag=pwn.college{UxZf5SYdJX_lnL-8XfeaC2fcN_2.dNzNyUDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/588af547-6cb1-4b9f-aa92-c55bd041c71e)

### Executing Files 
```
We use the chmod command to again give the execution permission to the flag file to the hacker user. We run chmod u+x /flag to give the user execution access to the flag file. 
flag=pwn.college{Qwd4V4FJss-7gX30JvbZzA5fvQj.dJTM2QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/07e2e08c-61d2-4e88-b92a-dc1357e2efab)

### Permission Tweaking Practice 
```
Each file has permissions for three users, the user itself, the group and others. The first three characters include the permissions for the user, the next three for the group and the remaining three for
other users. 
Round 1: 
Existing Permission:  rw-r--r--
Required Permission:  -w----r--
therefore we use the command chmod u-r,g-r /challenge/pwn to clear the first round. 
Round 2: 
Existing Permission: -w----r--
Required Permission: rw-rw-rw-
The required command to run is chmod u+r,g+rw,u+w /challenge/pwn to clear this round. 
Round 3: 
Existing Permission: rw-rw-rw-
Required Permission: r--rw-r--
Required command is chmod u-w,o-w /challenge/pwn. With this we go to the next round. 
Round 4: 
Existing Permission: r--rw-r--
Required Permission:  r--r--r--
Required command is chmod g+w /challenge/pwn to go to the next round. 
Round 5: 
Existing Permission: r--r--r--
Required Permission: r--r--rw-
The command is chmod o+w /challenge/pwn to go to the next round. 
Round 6: 
Existing Permission: r--r--rw-
Required Permission: ---r--rw-
The command entered is chmod u-r /challenge/pwn for the next round. 
Round 7: 
Existing Permission: ---r--rw-
Required Permission:  ------rw-
The required command is chmod g-r /challenge/pwn for the last round. 
Round 8: 
Existing Permission:  ------rw-
Required Permission: -w----rw-
The command required is chmod u+w /challenge/pwn. 
Round Flag: 
We have completed all the required rounds, now it is time to change the permissions of the flag. 
We use chmod u+r /flag to make it readable and execute cat /flag to get the flag. 
flag=pwn.college{46WW8RbQmm3ctvnN2s2EqY7yWGj.dBTM2QDL0MDO0czW}
```

### Permission Setting Practice 
```
Similar to the previous question, we use = to assign permissions to files. 
Current Permissions: rw-r--r--
Needed permissions: r---wxrw-
command: chmod u=r,g=wx,o=rw /challenge/pwn
Round 1 (of 8)!
Current permissions: r---wxrw-
Needed permissions of: --xrwx--x
command: chmod u=x,g=rwx,o=x /challenge/pwn
Round 2 (of 8)!
Current permissions: --xrwx--x
Needed permissions: r---w-r--
command: chmod u=r,g=w,o=r /challenge/pwn
Round 3 (of 8)!
Current permissions: r---w-r--
Needed permissions: -wxr-----
command: chmod u=wx,g=r,o=- /challenge/pwn
Round 4 (of 8)!
Current permissions: -wxr-----
Needed permissions: --x-wx---
command: chmod u=x,g=wx /challenge/pwn
Round 5 (of 8)!
Current permissions: --x-wx---
Needed permissions: rw--wx-w-
command: chmod u=rw,o=w /challenge/pwn
Round 6 (of 8)!
Current permissions: rw--wx-w-
Needed permissions: -wxr-x-wx
command: chmod u=wx,g=rx,o=wx /challenge/pwn
Round 7 (of 8)!
Current permissions: -wxr-x-wx
Needed permissions: -----xr--
command: chmod u=-,g=x,o=r /challenge/pwn
Current permissions of "/flag": ---------
command: chmod u=r /flag
now cat /flag to get the flag.
flag=pwn.college{0qID1tmTakWs18uyAliygjveQA3.dNTM5QDL0MDO0czW}
```

### The SUID bit 
```
This challenge explains us the importance of a suid bit, which can also be added using the chmod command. The suid bit,
represented with an additional s, gives us admin like privileges over a certain file. In this challenge, we give the 
suid bit /challenge/getroot and then run it to go to another root, where catting the file will give us the flag.
flag=pwn.college{s5CWLsrDP9-iYflAzY7Sbrcm8io.dNTM2QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/419aaa49-c033-43a1-a518-4af917eb038d)

