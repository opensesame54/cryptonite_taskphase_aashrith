# Comprehending_Commands Module 
### Cat, the command but not the flag 
```
**cat flag** to get the first flag. 
flag=pwn.college{8ore3TuJZRw9Z-zuhpFaQzqzcaM.dFzN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/ae292edc-4fae-495f-979b-617c9fed6810)

### Catting absolute paths 
```
Since we are getting the flag file by searching for it absolutely, we should do **cat /flag**. Before that we go to the '/' directory and then cat absolutely. 
flag=pwn.college{McQ0WvwPoGOgnm_3Qak3aRArzXz.dlTM5QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/1ae3a3be-7880-4d14-b466-1a9d25940474)

### more catting practice 
```
Basically, cd just to get an error and get the actual directory, then cat out the flag absolutely. 
flag=pwn.college{YSs4fQiFb8xxUTE_z-Xyr1uXFyU.dBjM5QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/e94763d2-7b2f-41fc-9490-751c1b2c882c)

(woah so many cars)

### grepping for the needle in a haystack 
```
Shows the usefullness of grep command, to find a particular line in thousands of lines. Since the flag always starts with pwn.college, we can say **grep pwn.college /challenge/data.txt** to get the flag. 
flag=pwn.college{8Nqegmf3C41aMBnmNTAlWrxF4T3.ddTM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/955fd420-2eb2-498a-976b-a1a3d705388a)

### Listing files 
```
Shows us how to use the ls command. Using ls, we can list out all the commands in /challenge. Initially I was trying to cat out the file, but just running it absolutely. 
flag=pwn.college{IMUtHgFkoAXXFaHGT7tkhCJh8Fm.dhjM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/e9411174-855c-4c6a-842b-284c069e2f7b)

### Touching files 
```
Learning to use the touch command. Using touch to create two files and then running /challenge/run gives us the flag. 
flag=pwn.college{8O-q3zrX8n4WibJu8SbJOnm5rgT.dBzM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/49dcba96-eb78-4acc-bfa1-3f59fae629d9)

### Removing files 
```
Learning to use the rm command. Create a file and then delete it. 
flag=pwn.college{4W7UJDroFcU7nIc0vdogfkt2KLM.dZTOwUDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/6edb65ac-16f6-4843-b338-0bdc1de8a227)

### Hidden files 
```
Using **ls -a** to show all the files in a directory. Since its told that the flag file is prepended with a '.', cat that file to get the flag. 
flag=pwn.college{YKjFDbfkPbKjbESr9GmiZuLIGCt.dBTN4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/8ff59ed2-f8c4-4e4d-8fde-86971b95f9c3)

### An epic filesystem quest 
```
Using hint after hint, eventually make way to the location of the flag. Places where the next clue is self destructible i.e one cannot cd into that directory, we can just ls the files of that directory and cat out the required file using its absolute path. 
```
![image](https://github.com/user-attachments/assets/712158b3-0814-4e69-a74d-9f6dfa464c93)
![image](https://github.com/user-attachments/assets/f6b5d235-99cf-496a-9d0f-b196ad095c2a)

### Making Directories 
```
Learning how to use the mkdir command. Using mkdir to create a new directory called /tmp/pwn, then using the touch command to create a new file inside this directory called college by **touch /tmp/pwn/college** and then running /challenge/run to get the flag. 
flag=pwn.college{MCrLv1b1g7Z3N_cQj9Pk-dIkv7D.dFzM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/75dfbc14-a792-4443-92f8-1e20fcf63b3c)

### finding files 
```
Learning the use of the find command. Used **find / -name flag** to search the entire system for the flag. Then tried each and every found match to get to the flag. 
flag=pwn.college{UY7F2GL_hYunoiV7tgAc1QBqHPB.dJzM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/3e3f5ed7-9084-48dd-ac3e-c775b6d9e559)

### Linking files 
```
This challenge teaches us the propery of links in linux. Using a symlink to get the contents of the flag into the /home/hacker/not-the-flag, we can access it by /challenge/catflag because it reads the contents of the /home/hacker/not-the-flag, which is acting as a symlink for the flag. 
flag=pwn.college{ImpQsc4GVnMPdwI1s5jjb-YV1g3.dlTM1UDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/e3bb36f1-0462-45ae-820d-0dca3103b87f)