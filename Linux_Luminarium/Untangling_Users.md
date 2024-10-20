# Untangling Users Module 
### Becoming root with su
```
We learn the use of su command in this challenge. This command gives us root privileges, provided we give the correct answer. In this, the password given to us is hack-the-planet. Catting the flag file once in the root gives us the flag which is: 
flag=pwn.college{Q-3-mxwzKeM5soTdopE3o3Dqwbm.dVTN0UDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/0c3b7a0c-5db8-4f34-8d20-d210080616fe)

### Other Users with su 
```
The su command, given the argument of a username, will switch to that user, provided we give the correct password. In ths case, we switch to the user zardus, with su zardus, and the password dont-hack-me. Once in the root of zardus, we run /challenge/run to get the flag. 
flag=pwn.college{o6E_Qvz8zEajHlheYlxOIDb0XG1.dZTN0UDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/d21ec3cf-6157-43f7-9a6c-714c4bbd8f38)

### Cracking Passwords
```
This challenge shows us the use of John the Ripper, a password cracker. With the help of a leaked shadow file, which stores passwords, john can find the password of certain users. In this, we run john /challenge/shadow-leak. 
Now john does his work, and gives us the password after working his way through the shadow file. Once we get the password, we su to zardus and run /challenge/run to get the flag. 
flag=pwn.college{MzF3QHpLd2nDRp-Ek_tT2J_zHde.ddTN0UDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/c7af9048-8d6d-4db6-bee9-0ef9da3e64de)

### Using sudo
```
Sudo command, or super-user do gives us all the privileges to run a file. In this challenge, we just sudo cat the flag to elevate privileges, and hence give us the flag!
flag=pwn.college{YKNWG35Coyxy1sK_1q1bByOK1UH.dhTN0UDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/85bffb4c-330f-46dd-b536-46ab62bef67d)