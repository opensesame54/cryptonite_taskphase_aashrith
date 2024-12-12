# Corrupted Png file
In this forensics challenge, we are given a corrupted png file. I digged online a bit to find if only the header bits were corrupted. Then I found this tool called tweakpng. Using this tool, I got to a point where the png wasn't corrupted anymore but still couldn't fathom anything from the image. 

A bit more digging online helped me find this tool called 010 hex editor and another tool called pngcheck, I found out that a bit called the interlace bit was set to a wrong value. Changing that bit, we get the flag. 

![image](https://github.com/user-attachments/assets/f5695417-9bba-4cfe-a041-8bea47647159)
010 Hex Editor to change the final interlace bit. 

![image](https://github.com/user-attachments/assets/afdbf514-5607-4c14-860e-f9e3929f152c)
Tweakpng to do the initial tweaking. 

![image](https://github.com/user-attachments/assets/868a1a77-8ba1-4327-854a-b73090f297d5)
Before chaning the interlace bit. 

After changing the interlace bit: 
![image](https://github.com/user-attachments/assets/1372a395-a488-41fc-a7da-e41ee914356b)