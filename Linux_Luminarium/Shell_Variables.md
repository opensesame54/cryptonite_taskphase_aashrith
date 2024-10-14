# Shell Variables Module 

### Printing Variables 
```
Using echo, we can get the shell to print out things, using echo along with $, we can print variables. To solve this challenge, we run echo $FLAG to get the flag. 
flag=pwn.college{8agZjY1OLLK8UgO-MNEsgPZacFQ.ddTN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/a3a810c6-6d5f-4a6b-9d79-6e346f6bc2d6)

### Setting Variables 
```
In this, we set the value of the variable PWN to COLLEGE to get the flag. 
flag=pwn.college{Au1vAJiiHim5EmO7YYuf0A1vg43.dlTN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/cfed2e66-4e3b-424b-9d0a-92c12b76d23f)

### Multi-Word Variables 
```
This challenge tells us that spaces are not proper syntax. To get the flag, we set PWN="COLLEGE YEAH". 
flag=pwn.college{8kdZtU1jxw_YgyCnf4-KjSXvEoL.dBjN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/6b5408c6-8a89-40e4-bc8c-a017ebaa7e31)

### Exporting Variables 
```
First, we set the value of the variables PWN to COLLEGE and vice versa, but we only export PWN. Then invoking /challenge/run with the PWN argument, we get the flag. 
flag=pwn.college{k14O0Y33N93y4p0mFd6G0B6pOwM.dJjN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/102cd7b2-39db-4213-bc78-1ab0931c2626)

### Printing Exported Variables 
```
This challenge tells us the use of the env command, to print out all the environment variables. This also gives us the flag.
flag=
```
![image](https://github.com/user-attachments/assets/0ef78154-dd4f-402e-abfe-aef321b97f46)

### Storing Command Output 
```
This challenge teaches us that we can direcly read the output of files into variables. We put the output of /challenge/run into the variable PWN and cat it out to get the flag. 
flag= pwn.college{ESEQ8d-ut_f4d7AtUdwk2ThTJ2r.dVzN0UDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/91a84907-0ae6-46ab-a26c-bdc60c695117)

### Reading Input 
```
We learn how to give input in this challenge, using the read command. The read takes an input to a variable. To get the flag we take the input of PWN using read and set it to college.
flag=pwn.college{wRaFpVazO0c82HdVz-MZ0Aq060L.dhzN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/0c0c5a7e-359b-49e9-bb9a-c0f32cacd31c)

### Reading Files 
```
In this  challenge, we redirect the output of /challenge/read_me into the variable PWN, using the redirect (<) operator to get the flag.
flag=pwn.college{whjAjvXAaEhvWUGZ5xvqU9E0LIK.dBjM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/3fb3c6c9-ba7e-46b6-96cf-1c2767a08f7f)

