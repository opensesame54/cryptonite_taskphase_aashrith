# Vault Door 3 Challenge 
Opening the challenge, we see a java code which breaks the password into 4 different parts. 
```java
import java.util.*;

class VaultDoor3 {
    public static void main(String args[]) {
        VaultDoor3 vaultDoor = new VaultDoor3();
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

    // Our security monitoring team has noticed some intrusions on some of the
    // less secure doors. Dr. Evil has asked me specifically to build a stronger
    // vault door to protect his Doomsday plans. I just *know* this door will
    // keep all of those nosy agents out of our business. Mwa ha!
    //
    // -Minion #2671
    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
        String s = new String(buffer);
        return s.equals("jU5t_a_sna_3lpm18g947_u_4_m9r54f");
    }
}
```
In the checkPassword method, we see that the password is being broken down into 4 parts and is encrypted. So reversing that logic and writing that code for the given .equals string, we get the flag.
```java
public class DecryptPassword {
    public static void main(String[] args) {
        String targetBuffer = "jU5t_a_sna_3lpm18g947_u_4_m9r54f";
        char[] password = new char[32];
        for (int i = 0; i < 8; i++) {
            password[i] = targetBuffer.charAt(i);
        }   
        for (int i = 8; i < 16; i++) {
            password[23 - i] = targetBuffer.charAt(i);
        }
        for (int i = 16; i < 32; i += 2) {
            password[46 - i] = targetBuffer.charAt(i);
        }
        for (int i = 31; i >= 17; i -= 2) {
            password[i] = targetBuffer.charAt(i);
        }
        System.out.println(new String(password));
    }
}
```
Running this program, we get the flag. 
flag=picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_79958f}