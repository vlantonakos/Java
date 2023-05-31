An Iterator is an object that can be used to loop through collections, like ArrayList and HashSet. 
It is called an "iterator" because "iterating" is the technical term for looping.
To use an Iterator, you must import it from the java.util package.


```
import java.util.ArrayList;
import java.util.Iterator;

public class Main {
  public static void main(String[] args) {
    ArrayList<Integer> numbers = new ArrayList<Integer>();
    numbers.add(12);
    numbers.add(8);
    numbers.add(2);
    numbers.add(23);
    Iterator<Integer> it = numbers.iterator();
    while(it.hasNext()) {
      Integer i = it.next();
      if(i < 10) {
        it.remove();
      }
    }
    System.out.println(numbers);
  }
}
```
OUTPUT:
[12, 23]
