# ASM 1 
Upon opening the file given in the challenge, we are given machine code. We need to find what happens to the value 0x2e0 in the register.

Machine code is read line by line. Our value is pushed into the stack. 

```
<+3>:	cmp    DWORD PTR [ebp+0x8],0x3fb
<+10>:	jg     0x512 <asm1+37>
```
this line is checked first, the value in our register is 736, and since it is less tan 0x3fb, the next operation (jump if greater) is not satisfied and it moves to the next compare operation. 

```
<+12>:	cmp    DWORD PTR [ebp+0x8],0x280
<+19>:	jne    0x50a <asm1+29>
```
This is the jne(jump not equal operation) which returns true in this case, so the conditional jump takes place and moves to line 29. 

```
<+29>:	mov    eax,DWORD PTR [ebp+0x8]
<+32>:	sub    eax,0xa
```

The value in our register is now moved to the eax register, and 0xa is subtracted from it, so the key is: 736-10, which in hexadecimal is ```0x2d6``` which is our flag. 


0x2e0 in decimal is 736, the content of our register is 736
On line 3, we compare 736 and 1019
moved 736 to eax, added 10 to it, so value of register is 746
returned 