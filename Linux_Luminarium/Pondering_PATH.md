# Pondering PATH module 
### The PATH variable 
```
Since the challenge says that running /challenge/run natively will delete the file, we first set PATH to empty, so that it cannot find the function related to PATH. Now, running /challenge/run will give us the flag since there is no other function mapped to it. 
flag=pwn.college{gtG6dxXzILEOPUz_a5lDfVCT3ss.dZzNwUDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/66e9c709-5cda-404c-88b0-44a5962514c0)

### Setting PATH
```
In this challenge, we set the PATH variable to the given directory which is /challenge/more-commands. Now, we can run /challenge/run which invokes win and gives us the flag. 
flag=pwn.college{oF5N9o3m-Qq1239XXKpk0meX44I.dVzNyUDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/a1d95623-f5ab-4727-9df8-f5ad3677e3e2)

### Adding Commands 
```
First, we create a win file, and put the location of the cat command and set it to invoke the /flag file. Once we do that, we change the permissions of the win file so that it is executable, and setting the PATH variable to the present directory, so when we invoke /challenge/run, it works in the present directory. This gives us the flag. 
flag=pwn.college{kJtvddL6K91qe4VhlUyKsbdlqXO.dZzNyUDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/1008e25d-17ee-4796-92c0-8d8c55b79b02)


### Hijacking Commands 
```
This challenge has two steps, first, we change the directory of rm so that PATH recognises that first instead of the actual rm command.This is done using PATH=~/:$PATH. This rm file doesn't need to have anything inside it, so we can leave it empty. We change the permissions of the rm file so that it can be executed using chmod, and once we run /challenge/run for the first time, we see that the PATH takes the duplicate rm command. Now, we edit this rm file to hijack the flag for us, by making it cat the file whenever we initiate /challenge/run. This way, we get the flag.
flag=pwn.college{cKlPPfk6q8puJoGMBel06oClGHA.ddzNyUDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/f3627813-f16f-470b-adf3-d21d64f2ad5e)

## The end.