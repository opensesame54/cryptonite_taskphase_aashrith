# File Globbing Module 
### Matching with * 
```
Since we're not allowed to use more than 4 characters, use cd /ch* to change directory to /challenge, then run /challenge/run to get the flag. 
flag=pwn.college{ka_KPWLJtGraRjP5KZ_Jyw2m5JT.dFjM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/d9ccb768-922a-48b9-bb49-bde2b3c99935)

### Matching with ?
```
With the help of ?, we can match a single character. In this we have to replace c and l with a ?, so the command we have to invoke is cd /?ha??enge to go to challenge and run /challenge/run to get the flag. 
flag=pwn.college{sUAMz03RK2Br4PGEUKYVmjJvVhb.dJjM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/2cae3605-a147-4a25-9924-8578eba12f9b)

### Matching with []
```
cd into /challenge/files and invoking /challenge/run with file_[bash] an argument to get the flag. 
flag=pwn.college{0ptrXMrSJX8ZtJmGVQYZEh7Yp6l.dNjM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/dc5c562f-66eb-4755-a86e-6e9a9ac54a1f)

### Matching paths with []
```
first cd into the home directory by cd ~ and then invoke the command /challenge/run with the parameter /challenge/files/file_[bash] to get the flag. 
flag=pwn.college{kA2dC_Wd_wIbp5xuccMHP3lPPy0.dRjM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/a764c460-f8b5-4510-84fe-8514a25bade1)

### Mixing Globs 
```
In this, we need to glob 3 files, with the requirement of it being 3 characters or less, so we can cd into /challenge/files and then we can run /challenge/run with the argument [cep]* so that it includes all the files starting with the letters c,e and p. 
flag=pwn.college{o6JERBi_8MZpkZkInkygd0hP1xx.dVjM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/b265ceb8-f3a7-4045-8524-555caffb4862)

### Exclusionary globbing
```
In this, we first cd into /challenge/files and then we invoke /challenge/run with the parameter [!pwn]* which represents all the files which dont start with pwn and the * fills the rest of the files. 
flag=pwn.college{g1SX0rnrRGjIHG_dtUa8s47B2Iv.dZjM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/46ec7ea1-74c5-4fc9-b705-99d6caf2aebc)