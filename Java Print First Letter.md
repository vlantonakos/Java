```
public class Main {

    public static void main(String[] args) {
        String sentence = "The quick brown fox jumps over the lazy dog";
        printFirstLetters(sentence);
    }

    static void printFirstLetters(String sentence) {
        String[] words = sentence.split(" ");

        for (String word : words) {
            if (!word.isEmpty()) {
                char firstLetter = word.charAt(0);
                System.out.print(firstLetter);
            }
        }
    }
}
```
OUTPUT:
Tqbfjotld
