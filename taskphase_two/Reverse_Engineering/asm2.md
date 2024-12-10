# ASM 2
Similar to the previous question, we have some assembly code, and this time, we have two arguments instead of one, they are: ```0xb,0x2e```. 

First, memory is allocated and the second argument is loaded and stored in the stack with this command. 

```asm
mov    eax,DWORD PTR [ebp+0xc]
mov    DWORD PTR [ebp-0x4],eax
```

Similarly, the second argument is also loaded and stored
```asm
mov    eax,DWORD PTR [ebp+0x8]
mov    DWORD PTR [ebp-0x8],eax
```
Next, an unconditional jump takes place with this command: 
```asm
jmp    0x509 <asm2+28>
```
Now, we jump into the loop with the compare operator ```jlp```, which is jump is less than or equal to. With this we understand that it is a while loop. 

so the while loop works something like this: 
```while 1st element is less than a certain value:
    add one to 0x4
    add 0x80 to the second value
```
based on this, I wrote a python code
```py
    e4 = int('0x2e', 16)
    e8 = int('0xb', 16)
    while e8 <= int('0x63f3', 16):
        e4 += int('0x1', 16)
        e8 += int('0x80', 16)
    print(hex(e4))
```
This prints the flag ```0xf6```