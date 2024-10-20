# Chaining Commands Module
### Chaining with Semicolons
```
A ; helps us chain 2 commands together. With this, we can specify two commands in the same line, just seperated by a semi-colon. We run /challenge/run ; /challenge/college, basically chaining them to get the flag. 
flag=pwn.college{I2tC-yPeoYr0kO1r3SaKnZY5tvd.dVTN4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/a47f9007-4053-4b41-8ae3-9cc28a55ddff)

### Your first shell script 
```
Creating my first shell script, First, we create a file called x.sh. I used vim to create the file, using vi x.sh.
After this, we type the commands line by line, first /challenge/run and /challenge/college. When we run this file using bash x.sh, we get the flag. 
Catting x.sh file also gives us the content inside it. 
flag=pwn.college{gmcRSvIMoJ80GjabX15kENo-S2V.dFzN4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/37339fb9-dbf8-4b70-b225-9d27df17ebe3)

### Redirecting Script output 
```
As we learnt in the previous modules, we can redirect the output of file using the pipe (|) operator. In this challenge, we use the already created x.sh file with both the required commands. Then, to pipe the output, we do bash x.sh | /challenge/solve, which gives us the flag. 
flag=pwn.college{wAL5TyOjeV-KjSBkPClqLxUFb1h.dhTM5QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/58cd5be4-d51e-4327-a7de-48648478683e)

### Executable Shell Scripts 
```
We create a new file called y.sh, and write the command /challenge/solve to it. Now, we set the permission of this file to execute (I set it to all three) and since it is already in the home directory, we use ./y.sh to run it to get the flag. 
flag=pwn.college{cmteyiKfTH3cBGenZ8QYlMtld2r.dRzNyUDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/58cd5be4-d51e-4327-a7de-48648478683e)



