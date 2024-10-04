# Pondering Paths Module 
### The Root 
```
Used the absolute path of **/pwn** to get the flag
flag=pwn.college{8AyjpOSAfUdG7IafRfJPVSvNBG7.dhzN5QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/4a809ef1-94a7-4e7b-8da0-831e70f344d2)

### Program and Absolute paths
```
Invoked the absolute path of **/challenge/run** to get the flag. 
flag=pwn.college{c9HfB1y14RjfmxxC5WGeifuYQdl.dVDN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/3c133cc0-1543-43bf-8dff-3bd67996fe8e)

### Position thy self 
```
Invoked the **/challenge/run** from the home directory, where I was directed to go to **/usr/share/doc** using cd, and then after cd'ing into that directory, invoked the absolute path again. 
flag=pwn.college{4M3HKlEuI9QpKuSjrgwlliBCu1i.dZDN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/25549254-dd6b-4769-9708-571e1661582f)

### Position Elsewhere
```
Same procedure as the previous question. 
flag=pwn.college{8tMoTXhCUze436KncRNTApBB-2b.dhDN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/1bb1dc70-a25d-48f8-8b14-bc03a2c6b6d6)

### Implicit Relative paths, from /
```
As directed, using cd went to the **/** directory, then invoked the folder relatively, which is **challenge/run**
flag=pwn.college{wvYVajLy1zGZ5D48gN2cxa-kswi.dlDN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/c1dd90bc-9908-4f13-b2fa-e8ccfe4ff140)

### Explicit relative paths, from /
```
Similar to the last question but this time used **.** to specify the present directory. Then relatively ran the file using the command **./challenge/run**. 
flag=pwn.college{47u_ZohqaYxegxmTmCGsUijoaIc.dBTN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/a32343f7-0920-43ef-af04-50a8a34ac617)

### implicit relative path 
```
As the question directed, I ran the relative path from the **/challenge** directory. Then specified the pwd (present working directory) by using **.**. Command is **./run**. 
flag=pwn.college{0hPUMvoeXFFigXfPReKHycTkRPO.dFTN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/678a14e6-d9e8-47f7-abf0-e1d66ef7bbae)

### home sweet home
```
Adhereing to the given conditions that the path should be absolute and that it must be inside the home directory **~**, and the argument must be less than 3 characters long, Copied the flag file onto a file in the home directory using **~/f** which accepts the third condition. The used command is **/challenge/run ~/f**
flag=pwn.college{E-GJigxEL1toj0kwiBBw0FFGtdU.dNzM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/c338a036-4e8b-41b1-abb8-4ee50f6086d3)

