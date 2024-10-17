# Processes and Jobs Module 
### Listing Processes 
```
first, we cd into /challenge, then list out all the processes using ps aux, and then run the renamed run file to get the flag. 
flag=pwn.college{kCUDQKCV3Vhtj1XlzEdubOqIAxr.dhzM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/fe1807f8-8d11-47cc-8d17-89526c863127)

### Killing Processes
```
In this, we use ps -e to list out all the processes, and then kill the sleep process using the kill command to get the flag. 
flag=pwn.college{IOLilh-5fhRoKoK3KK_jOsY_y1R.dJDN4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/ab024468-91a1-4d3c-b94b-cf5a39be3ad6)

### Interrupting Processes 
```
Teaches us how to use ctrl+C to stop processes. First we run /challenge/run and then run ctrl+c to get the flag.
flag=pwn.college{o6B2NRUF5TtANIsD-Y28ApsbZC2.dNDN4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/782444a1-9874-4c1e-a92a-32a9f7b0ed18)

### Suspending Processes 
```
We use ctrl+z to suspend processes. Similarly, we invoke /challenge/run and run ctrl+z to get the flag. 
flag=pwn.college{QePWMj3egXCxgXLb9DC-tcOVVEb.dVDN4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/e4f52ae4-a7f0-428d-89eb-365bef81cc4d)

### Resuming Processes 
```
Firstly, we invoke /challenge/run and then suspend it using ctrl+z, and then we use fg (foreground) to resume /challenge/run to get the flag. 
pwn.college{4LEGoO9lAvk_EpOpWHtTYZDu5Uy.dZDN4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/0ba3fde9-917c-4d22-9613-26d994db160f)

### Backgrounding Processes
```
First, we normally run /challenge/run and suspend the process and resume it in the background using the bg command and start another instance of /challenge/run in the foreground to get the flag. 
flag=pwn.college{4NNKqX4GfKVVZ2-O39By__9_kd5.ddDN4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/8b5dbb40-abf2-4b9e-bd44-0c2cb31648c1)

### Foregrounding Processes 
```
We normally invoke /challenge/run and then use ctrl+z to suspend it and then use bg to resume it in the background. And then we get it to foreground by using fg /challenge/run, we get the flag after foregrounding this process. 
flag=pwn.college{8Ij7PHN9ppBxJ5lVm_mUOBKpy3p.dhDN4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/f35ee7f2-0e8a-4fcf-b3b7-282afb7b8d98)

### Starting Processes
```
This challenge tells us that we can start processes in the background by just appening an & as an argument. Here, starting /challenge/run in the background gets us the flag. 
flag=pwn.college{w7OqG5JAYf7SV2RptFgmFZqtFvh.dlDN4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/bb64ea0e-8f28-42fd-8b75-0cd3889f4c6a)

### Process Exit Codes 
```
In this, we learn to read the end codes of different commands. We run /challenge/get-code to start the challenge, and then echo $? to get the code, which is 87 in this case, then we invoke /challenge/run with 87 as an argument to get the code. 
flag=pwn.college{4iZOQUIv4rF7kac2gkhv4G8HYt3.dljN4UDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/60e6de99-cd64-4814-b375-532a440a1aa0)