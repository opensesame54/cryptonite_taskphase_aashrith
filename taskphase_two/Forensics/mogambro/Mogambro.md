# Mogambro challenges (BITSCTF)

## Access Granted! 
Opening the mogambro zip file, we have three files, a memory dump file, an ad1 image and a pcap file. 
For the first question, we are given the following hint. 
```First things first. MogamBro is so dumb that he might be using the same set of passwords everywhere, so lets try cracking his PC's password for some luck.
```
So, to get the passwords stored by mogambro, we need to know where passwords are stored in a windows system. Passwords are stored in a SAM database, which cannot be accessed when the system is running. This can be accessed by accessing the windows hashdump. To use the memory dump given to us, we need to use a tool called volatility3 (installing this was such a pain). 

To use this tool, we run 
```py vol.py -f 'memdump location' windows.hashdump```

This will give us the following hashes, which then we can use a password cracker to get the flag. 

![image](https://github.com/user-attachments/assets/aef0b428-6974-4a09-8706-f2bb155c507d)

```flag=BITSCTF{adolfhitlerrulesallthepeople}```

## 0.69 Day 
For this challenge, we need to use an application called FTK imager, so we can inspect the ad1 image file. Using this application, we can see what files are there in mogambro's system. 
