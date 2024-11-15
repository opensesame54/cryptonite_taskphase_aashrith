# Vault-Door-1 Challenge 

Opening the java code provided with the challenge, we see that the code is giving us the flag, but the positions are just scrambled. 

So, we write the code to descramble the code and give us the flag 
```java
public class PasswordChecker {

    public static void main(String[] args) {
        char[] passwordChars = new char[32];

        
        passwordChars[0]  = 'd';
        passwordChars[1]  = '3';
        passwordChars[2]  = '5';
        passwordChars[3]  = 'c';
        passwordChars[4]  = 'r';
        passwordChars[5]  = '4';
        passwordChars[6]  = 'm';
        passwordChars[7]  = 'b';
        passwordChars[8]  = 'l';
        passwordChars[9]  = '3';
        passwordChars[10] = '_';
        passwordChars[11] = 't';
        passwordChars[12] = 'H';
        passwordChars[13] = '3';
        passwordChars[14] = '_';
        passwordChars[15] = 'c';
        passwordChars[16] = 'H';
        passwordChars[17] = '4';
        passwordChars[18] = 'r';
        passwordChars[19] = '4';
        passwordChars[20] = 'c';
        passwordChars[21] = 'T';
        passwordChars[22] = '3';
        passwordChars[23] = 'r';
        passwordChars[24] = '5';
        passwordChars[25] = '_';
        passwordChars[26] = 'f';
        passwordChars[27] = 'f';
        passwordChars[28] = '6';
        passwordChars[29] = '3';
        passwordChars[30] = 'b';
        passwordChars[31] = '0';

        
        for (int i = 0; i < passwordChars.length; i++) {
            System.out.print(passwordChars[i]);
        }
    }
}

```

Reindexing the characters and printing it, we get the flag. 

```flag=picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_ff63b0}```