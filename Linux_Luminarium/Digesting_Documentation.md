# Digesting Documentation Module
### Learning from Documentation 
```
Just implement **/challenge/challenge --giveflag** to get the flag. 
flag=pwn.college{0Qb23XO0ijZvEGUG5yu2KAAXzGn.dRjM5QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/201f3050-1bad-4e60-a2f1-345043b551a9)
### Learning Complex usage 
```
To get the flag, invoke /challenge/challenge with the printfile argument. So the command used will be **/challenge/challenge --printfile /flag** 
flag=pwn.college{Ug_Q4eYj-tZsCyHoJAdiMxZe7tY.dVjM5QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/584840b8-cdeb-44d1-8b9b-5b5bf2a6fc21)
### Reading Manuals 
```
First, invoking man challenge to get the description, and then using the details in that description to get the flag. 
flag=pwn.college{o7Y_1eUKBDl1V0aL2oqHG54BUCn.dRTM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/30532d92-7a80-4b76-8298-bf7800950be7)
### Searching manuals 
```
Firstly, using man challenge to get the list of all arguments, then forward searchin using / to search for the flag keyword, then invoking the right parameter with /challenge/challenge to get the flag. 
flag= pwn.college{wa4Y9Ug535QSIC7h8-cMBUzxOaa.dVTM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/8bdee2b2-acc7-402f-9e33-303a01892587)
![image](https://github.com/user-attachments/assets/6bf23cb5-5cdc-4ba4-810b-b6d68b570d70)

### Searching for manuals
```
This challenge makes us use the man man command to find the correct argument to invoke with /challenge/challenge. First, to print the flag we have to use man -k challenge to get the correct argument, in this case which is iygypbhjer, and when searching for this argument in the manual, we get the argument to invoke the flag with. 
flag=pwn.college{I3iygypbhjJeVrdWQcHtuUbWV0-.dZTM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/06e4bb6f-a70d-4c9e-b3bc-f18cf6b80a03)
![image](https://github.com/user-attachments/assets/30fbe5ad-889e-4d13-b54f-791dd5b77ac8)
![image](https://github.com/user-attachments/assets/992bb933-991a-4317-beb2-f99cc956baed)

### Helpful Programs 
```
This problem teaches us the importance of the --help command, invoking it as a parameter with /challenge/challenge, 
we get the instruction to print, and then invoking /challenge/challenge -p, we get the secret value which in this case is 54, and using that as a parameter with -g, we get the flag. 
flag= pwn.college{c0AKQkRDDzncgxbKQVdWdy5hiNH.ddjM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/a05a7945-905b-45d3-afdb-155e1619bdf3)

### Help for Bulletins 
```
In this problem, invoking help with challenge as a paramter, which gives us the secret value to get the flag. 
flag=pwn.college{gZFN8JQ2F-NTuQ64_ozWL2vcJRN.dRTM5QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/a4b81e11-a62e-43fe-bada-e3e7ce0b1fc4)