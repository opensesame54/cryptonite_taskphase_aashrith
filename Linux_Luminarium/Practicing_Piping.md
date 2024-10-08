# Practicing Piping Module 
### Redirecting Output 
```
Use echo PWN > COLLEGE to write pwn to the file COLLEGE to get the flag. 
flag=pwn.college{Q5lQplb03nT4PgLC1hm4jBLGOqk.dRjN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/98c56dec-e739-41e2-8394-443a3838788f)

### Redirecting More Output
```
Like we used echo to send text to a file, we can copy the contents of a file. So by running /challenge/run > myflag, the contents of /challenge/run are copied into myflag, and now running myflag file, we get the flag. 
flag= pwn.college{8fH2lzHY2pgIblVXdb4jOtR-gSD.dVjN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/8fcbfacc-7d36-4914-b46e-fff335652701)

### Appening output 
```
Basically, when we just use > to write files, it deletes the previous instance of that file and creates a new file, this can be avoided if we use **>>**, which is the append mode. So appending the contents of the file /challenge/run to ~/the-flag will give us the flag. \
flag=pwn.college{YNETuCydkkTCyCE6riHse4i8MDd.ddDM5QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/81cda8f4-1078-4d88-b533-4595245903cb)

### Redirecting Errors 
```
In this, we are redirecting an error using a file descriptor, which looks like this: 2> (this is for an error). So we are copying the contents of /challenge/run into myflag and taking all the errors which might occur into a file called instructions. So the command will be **/challenge/run > myflag 2> instructions**. After this, catting myflag will give us the flag. 
flag=pwn.college{0c1-kN-3RCUevG_nb4ld-z4ViJ_.ddjN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/e9627aa4-cb52-4ba9-866a-88f7e1152c03)

### Redirecting Input 
```
Similar to how we can input stuff into files, we can also redirect files into the standard input using <. So, in this case echoing COLLEGE to a file called PWN and then redirecting it to /challenge/run, we get the flag. 
flag=pwn.college{YBkXFqY36AGgs_pganpOipDUbSb.dBzN1QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/d1bc399a-7cb5-491c-8001-9c7e002a33ad)

### Grepping Stored Results 
```
First we redirect the output out /challenge/run to /tmp/data.txt, which produces a prompt. Now grepping /tmp/data.txt for pwn.college, we get the flag. 
flag=pwn.college{Y8PoakcDyse-_KEXcVsSe2DDrsm.dhTM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/bb68e253-cdd0-4175-8aff-67a08dc11bf7)\

### Grepping Live output 
```
This challenge teaches us the use of the pipe operator (|). So we can invoke /challenge/run and grep for the flag at the same time. /challenge/run | grep pwn.college will give us the flag. 
flag=pwn.college{cnHv3NKe2dSuIpdJCA8wdxwg55r.dlTM4QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/519f54f5-b583-467f-928e-d41ad66ee597)

### Grepping errors 
```
In this, we pass the error through the expression 2>&1 and then use the pipe operator to grep for the flag. 
flag=pwn.college{UXZlIP0MEHNcSLHh5mgYvk0dPTR.dVDM5QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/95310980-a36f-4e80-bfb1-82cf604a35c4)

### Duplicating Piped data with tee
```
Shows the usage of the tee command. Like in golf, tee is used for supporting the ball, similarly, the tee command copies the input into another file and another copy to the specified command. Running /challenge/run | tee pwn_output | /challenge/college, we create a folder called pwn_output which gives us a description on how to run /challenge/run. Using this information, we invoke the proper method to run /challenge/run to get the flag. 
flag=pwn.college{8P7E1w-TJzUfnpti3HJ_ht0RfSM.dFjM5QDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/aaf1dc84-8a16-4480-b032-3759aa552496)

### Writing to multiple programs 
```
In this, we duplicate the input of the program /challenge/hack into two programs with the use of the tee command. 
So the command we invoke will be /challenge/hack | tee >( /challenge/the ) >( /challenge/planet )
here, the pipe operator sends the output of /challenge/hack to the tee function, and tee duplicates this output to both the files. 
flag= pwn.college{QYzj1qMqIhvcv2JPj6ho-wQYluL.dBDO0UDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/af06e28b-f143-45d2-aa18-6ac1866cf155)

### Split piping stderr and stdout 
```
This challenge teaches us the method of redirection. We pipe the stdout and stderr seperately into their respective files. So the command will be /challenge/hack > >( /challenge/planet ) 2> > ( /challenge/the ) to get the flag. 
flag=pwn.college{AJ98VIAcNcV1tPPUIgOoQoQRO5S.dFDNwYDL0MDO0czW}
```
![image](https://github.com/user-attachments/assets/0c70f6a8-f89d-4a21-b006-080a31132f52)
