```
import java.util.Scanner;

public class Main {
	
	public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String input = scanner.nextLine();
        
        if (hasVowel(input)) {
            System.out.println("The string contains at least one vowel.");
        } else {
            System.out.println("The string does not contain any vowel.");
        }
    }
	
	public static boolean hasVowel(String str) {
        str = str.toLowerCase();  // convert string to lowercase for case-insensitive comparison
        
        for (int i = 0; i < str.length(); i++) {
            char ch = str.charAt(i);
            if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
                return true;  // a vowel is found, return true
            }
        }
        
        return false;  // no vowel is found, return false
    }
}
