```
import java.io.*;
import java.util.Arrays;

public class Main {

    public static void main(String[] args) {
        String str = "racecar";
        if (isPalindrome(str)) {
            System.out.println(str + " is a palindrome.");
        } else {
            System.out.println(str + " is not a palindrome.");
        }
    }

    static boolean isPalindrome(String str) {
        str = str.toLowerCase(); // Convert the string to lowercase for case-insensitive comparison
        int left = 0;
        int right = str.length() - 1;

        while (left < right) {
            if (str.charAt(left) != str.charAt(right)) {
                return false; // Characters at symmetric positions don't match, not a palindrome
            }
            left++;
            right--;
        }

        return true; // All characters match, it is a palindrome
    }
}
```
OUTPUT:
racecar is a palindrome.
