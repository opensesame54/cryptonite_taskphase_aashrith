# Vault Door 7 Challenge 
In this challenge, the code takes the input of the flag string, converts it into ascii, and then converts that converted ascii code into binary. Now these binary digits, when placed 4 at a time, we get the integer digits, which are checked with the password integer digits. To get the flag, we have to convert the password integer digits back to the original character format. 

The code given to us: 
```java
import java.util.*;
import javax.crypto.Cipher;
import javax.crypto.spec.SecretKeySpec;
import java.security.*;

class VaultDoor7 {
    public static void main(String args[]) {
        VaultDoor7 vaultDoor = new VaultDoor7();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
	String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
	if (vaultDoor.checkPassword(input)) {
	    System.out.println("Access granted.");
	} else {
	    System.out.println("Access denied!");
        }
    }

    // Each character can be represented as a byte value using its
    // ASCII encoding. Each byte contains 8 bits, and an int contains
    // 32 bits, so we can "pack" 4 bytes into a single int. Here's an
    // example: if the hex string is "01ab", then those can be
    // represented as the bytes {0x30, 0x31, 0x61, 0x62}. When those
    // bytes are represented as binary, they are:
    //
    // 0x30: 00110000
    // 0x31: 00110001
    // 0x61: 01100001
    // 0x62: 01100010
    //
    // If we put those 4 binary numbers end to end, we end up with 32
    // bits that can be interpreted as an int.
    //
    // 00110000001100010110000101100010 -> 808542562
    //
    // Since 4 chars can be represented as 1 int, the 32 character password can
    // be represented as an array of 8 ints.
    //
    // - Minion #7816
    public int[] passwordToIntArray(String hex) {
        int[] x = new int[8];
        byte[] hexBytes = hex.getBytes();
        for (int i=0; i<8; i++) {
            x[i] = hexBytes[i*4]   << 24
                 | hexBytes[i*4+1] << 16
                 | hexBytes[i*4+2] << 8
                 | hexBytes[i*4+3];
        }
        return x;
    }

    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        int[] x = passwordToIntArray(password);
        return x[0] == 1096770097
            && x[1] == 1952395366
            && x[2] == 1600270708
            && x[3] == 1601398833
            && x[4] == 1716808014
            && x[5] == 1734304867
            && x[6] == 942695730
            && x[7] == 942748212;
    }
}
```

So now, out byte array will include these 8 integer numbers. Using bitwise operations, we get 4 bytes from each integer and convert it to characters. 

The reverse engineered code: 
```java
public class VaultDoor7Cracker {
    public static void main(String[] args) {
        int[] targetInts = {
            1096770097, 1952395366, 1600270708, 1601398833,
            1716808014, 1734304867, 942695730, 942748212
        };

        StringBuilder passwordBuilder = new StringBuilder();

        for (int num : targetInts) {
            
            char c1 = (char) ((num >> 24) & 0xFF);
            char c2 = (char) ((num >> 16) & 0xFF);
            char c3 = (char) ((num >> 8) & 0xFF);
            char c4 = (char) (num & 0xFF);

            passwordBuilder.append(c1).append(c2).append(c3).append(c4);
        }

        String password = passwordBuilder.toString();
        System.out.println("Recovered password: picoCTF{" + password + "}");
    }
}

```

flag: picoCTF{A_b1t_0f_b1t_sh1fTiNg_dc80e28124}