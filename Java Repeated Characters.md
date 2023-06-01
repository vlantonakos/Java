```
public class Main {

    public static void main(String[] args) {
        String str = "Hello World";
        boolean hasRepeatedCharacters = hasRepeatedCharacters(str);
        
        if (hasRepeatedCharacters) {
            System.out.println("The string contains repeated characters.");
        } else {
            System.out.println("The string does not contain repeated characters.");
        }
    }
    
    static boolean hasRepeatedCharacters(String str) {
        boolean[] charSet = new boolean[128]; // Assuming ASCII characters
        
        for (int i = 0; i < str.length(); i++) {
            char c = str.charAt(i);
            if (charSet[c]) {
                return true; // Found a repeated character
            }
            charSet[c] = true;
        }
        
        return false; // No repeated characters found
    }
}
```
OUTPUT:
The string contains repeated characters.
