# Inferius Prime 
We are given a python code, and a text file with our values. To get the flag, we need to find the private key using pow(e,-1,phi(n)).
Once we get the private key, we can do pow(ct,d,n) and convert it to bytes to get the flag. 

![image](https://github.com/user-attachments/assets/519acae7-d4e9-48a6-bcfa-facd8b814ba8)

```
flag=crypto{N33d_b1g_pR1m35}
```